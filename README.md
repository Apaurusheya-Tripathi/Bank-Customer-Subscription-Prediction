{
 "cells": [
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "# Bank Marketing with Machine Learning"
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "## Introduction"
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "### Using Machine Learning to Predict Subscription to Bank Term Deposits for Clients with Scikit-Learn\n",
    "\n",
    "Marketing to potential clients has always been a crucial challenge in attaining success for banking institutions. It’s not a surprise that banks usually deploy mediums such as social media, customer service, digital media and strategic partnerships to reach out to customers. But how can banks market to a specific location, demographic, and society with increased accuracy? With the inception of machine learning - reaching out to specific groups of people have been revolutionized by using data and analytics to provide detailed strategies to inform banks which customers are more likely to subscribe to a financial product. In this project on bank marketing with machine learning, I will explain how a particular Portuguese bank can use predictive analytics from data science to help prioritize customers which would subscribe to a bank deposit.\n",
    "\n",
    "The data set is based off the direct marketing campaigns of a Portuguese banking institution. These marketing campaigns were based on phone calls. More than one contact to a client was required, in order to know if the product (bank term deposit) was subscribed by a client or not. The classification goal is to predict if a client will subscribe to the bank term deposit (yes/no).\n",
    "\n",
    "The dataset contains 21 columns including the output (y). I am going to discard the output column and use the remaining columns to find the most relatable independent variables (x) that will be able to predict if a customer will subscribe to a bank deposit or not."
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "## Dataset"
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "### Input variables:\n",
    "\n",
    "1 - age (numeric)\n",
    "\n",
    "2 - job : type of job (categorical: 'admin.','blue-collar','entrepreneur','housemaid','management','retired','self-employed','services','student','technician','unemployed','unknown')\n",
    "\n",
    "3 - marital : marital status (categorical: 'divorced','married','single','unknown'; note: 'divorced' means divorced or widowed)\n",
    "\n",
    "4 - education (categorical: 'basic.4y','basic.6y','basic.9y','high.school','illiterate','professional.course','university.degree','unknown')\n",
    "\n",
    "5 - default: has credit in default? (categorical: 'no','yes','unknown')\n",
    "\n",
    "6 - housing: has housing loan? (categorical: 'no','yes','unknown')\n",
    "\n",
    "7 - loan: has personal loan? (categorical: 'no','yes','unknown')\n",
    "\n",
    "### Related with the last contact of the current campaign:\n",
    "\n",
    "8 - contact: contact communication type (categorical: 'cellular','telephone') \n",
    "\n",
    "9 - month: last contact month of year (categorical: 'jan', 'feb', 'mar', ..., 'nov', 'dec')\n",
    "\n",
    "10 - day_of_week: last contact day of the week (categorical: 'mon','tue','wed','thu','fri')\n",
    "\n",
    "11 - duration: last contact duration, in seconds (numeric). Important note: this attribute highly affects the output target (e.g., if duration=0 then y='no'). Yet, the duration is not known before a call is performed. Also, after the end of the call y is obviously known. Thus, this input should only be included for benchmark purposes and should be discarded if the intention is to have a realistic predictive model.\n",
    "\n",
    "### Other attributes:\n",
    "\n",
    "12 - campaign: number of contacts performed during this campaign and for this client (numeric, includes last contact)\n",
    "\n",
    "13 - pdays: number of days that passed by after the client was last contacted from a previous campaign (numeric; 999 means client was not previously contacted)\n",
    "\n",
    "14 - previous: number of contacts performed before this campaign and for this client (numeric)\n",
    "\n",
    "15 - poutcome: outcome of the previous marketing campaign (categorical: 'failure','nonexistent','success')\n",
    "\n",
    "### Social and economic context attributes:\n",
    "\n",
    "16 - emp.var.rate: employment variation rate - quarterly indicator (numeric)\n",
    "\n",
    "17 - cons.price.idx: consumer price index - monthly indicator (numeric) \n",
    "\n",
    "18 - cons.conf.idx: consumer confidence index - monthly indicator (numeric) \n",
    "\n",
    "19 - euribor3m: euribor 3 month rate - daily indicator (numeric)\n",
    "\n",
    "20 - nr.employed: number of employees - quarterly indicator (numeric)\n",
    "\n",
    "### Output variable (desired target):\n",
    "\n",
    "21 - y - has the client subscribed a term deposit? (binary: 'yes','no')\n",
    "\n",
    "Source:https://archive.ics.uci.edu/ml/machine-learning-databases/00222/ \n",
    "\n",
    "Dataset has 40,000+ rows of data."
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "### In this project I will demonstrate how to build a model predicting clients subscribing to a bank's term deposit in Python using the following steps:\n",
    "\n",
    "-data exploration\n",
    "\n",
    "-feature engineering\n",
    "\n",
    "-building training/validation/test samples\n",
    "\n",
    "-model selection\n",
    "\n",
    "-model evaluation"
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "# Project Definition"
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "The classification goal is to predict if a client will subscribe to the bank term deposit (yes/no).\n"
   ]
  }
