# MACHINE LEARNING PROJECT
# URL BASED PHISHING WEBSITE DETECTION 
![image](https://github.com/Tanwar-12/PHISHING-WEBSITE-DETECTION/assets/110081008/40af9366-64e0-4a34-adbc-db3261053861)![image](https://github.com/Tanwar-12/PHISHING-WEBSITE-DETECTION/assets/110081008/901a42a2-833c-4188-84dd-1694017b5368)



## 1.TASK: BINARY CLASSFICATION
## 2.INTRODUCTION:
*The Internet has become an indispensable part of our life, However, It also has provided opportunities to anonymously perform malicious activities like Phishing. Phishers try to deceive their victims by social engineering or creating mockup websites to steal information such as account ID, username, password from individuals and organizations. Although many methods have been proposed to detect phishing websites, Phishers have evolved their methods to escape from these detection methods. One of the most successful methods for detecting these malicious activities is Machine Learning. This is because most Phishing attacks have some common characteristics which can be identified by machine learning methods.*
## 3. BUSINESS CASE: PREDCIT THE WEBSITE URL IT IS FAKE OR SAFE.

## 4.PYTHON IMPLEMENTATION
## 5.LOAD THE DATASET
###  **ABOUT DATASET**
* 1 means legitimate
* 0 is suspicious
* -1 is phishing

* The dataset is borrowed from Kaggle, https://www.kaggle.com/eswarchandt/phishing-website-detector .

* A collection of website URLs for 11000+ websites. Each sample has 30 website parameters and a class label identifying it as a phishing website or not (1 or -1).

* The overview of this dataset is, it has 11054 samples with 32 features. Download the dataset from the link provided.
  
* ## 6.**DOMAIN ANALYSIS**:
**1.UsingIP**: Check if the URL contains an IP address instead of a domain name. Phishing sites often use IP addresses to disguise their true identity.

**2.LongURL**: Longer URLs might be associated with phishing sites. Phishers sometimes use long, convoluted URLs to obfuscate the true destination.

**3.ShortURL**: The presence of shortened URLs might indicate phishing. Shortened URLs can hide the true destination, which may be used by phishers.

**4.Symbol@**: Check for the presence of '@' symbols in the domain name. Legitimate domain names typically do not contain '@' symbols, so their presence may indicate phishing.


**5.Redirecting//**: Look for multiple consecutive forward slashes ('//') in the URL, which could indicate redirection. Phishing sites often use redirection to mimic legitimate websites.

**6.PrefixSuffix**:  Analyze whether the domain name contains prefixes or suffixes (e.g., hyphens) that are commonly associated with phishing sites.

**7.SubDomains**: Check the number of subdomains in the URL. Phishing sites may use numerous subdomains to mimic legitimate domains or to create a false sense of security.

**8.HTTPS**:  Determine the prevalence of HTTPS in URLs. Legitimate websites increasingly use HTTPS for secure communication, so the absence of HTTPS may indicate a potential phishing site.

**9.DomainRegLen**: Investigate the length of time since domain registration. Phishing sites may use newly registered domains to avoid detection.


**10.UsingPopupWindow**: The presence of popup windows might indicate phishing attempts.

**11.IframeRedirection**: Check if the website uses iframe redirection, which can be a technique used in phishing.

**12.AgeofDomain**: Analyze the age of the domain. Phishing sites may frequently use newly registered domains.

**13.DNSRecording**: Check for DNS recording. Phishing sites may not have proper DNS records.

**14.WebsiteTraffic**: Higher website traffic might indicate a legitimate website, but this feature alone may not be conclusive.

**15.PageRank**: Analyze the PageRank of the website. Higher PageRank might indicate legitimacy, but it can be manipulated.

**16.GoogleIndex**: Check if the website is indexed by Google. Lack of indexing might indicate a new or suspicious website.

**17.LinksPointingToPage**:  The number of links pointing to the page might indicate legitimacy if coming from reputable sources.

**18.StatsReport**: The presence of statistical reports might indicate a legitimate website.

**19.Class**: The "class" feature likely represents the target variable in your dataset, indicating whether each entry is classified as a phishing website or a legitimate one.
### 7.BASIC CHECKS

## 8.EXPLORATORY DATA ANALYSIS
![image](https://github.com/Tanwar-12/PHISHING-WEBSITE-DETECTION/assets/110081008/3fca3c1d-0ccd-449a-b1c2-507e31881df6)

![image](https://github.com/Tanwar-12/PHISHING-WEBSITE-DETECTION/assets/110081008/1272acaf-5258-401d-850f-139000b07c74)
![image](https://github.com/Tanwar-12/PHISHING-WEBSITE-DETECTION/assets/110081008/64ed4220-8be2-49f2-bc20-b9e49ad04cb1)
![image](https://github.com/Tanwar-12/PHISHING-WEBSITE-DETECTION/assets/110081008/7e41415d-ef8f-4078-827b-abb4a78795dd)


![image](https://github.com/Tanwar-12/PHISHING-WEBSITE-DETECTION/assets/110081008/e99cc639-f324-4294-8d3c-456d27b31e61)

## MODEL CREATION & EVALUATION
### DEFINE INDEPENDENT AND DEPENDENT VARIABLE
### SPLIT TRAINING AND TESTING DATA
* Training Accuracy : 0.9273823884197828
* Testing Accuracy : 0.9316208393632417
## MODEL BUILDING
### 1. SUPPORT VECTOR CLASSIFIER

**CLASSIFICATION REPORT** 

              precision    recall  f1-score   support

         Bad       0.90      0.94      0.92      1173
        Good       0.95      0.93      0.94      1591

    accuracy                           0.93      2764
   macro avg       0.93      0.93      0.93      2764
weighted avg       0.93      0.93      0.93      2764

### DECISION TREE
* Training Accuracy : 0.9218335343787696
* Testing Accuracy : 0.9251085383502171

**CLASSIFICATION REPORT**

              precision    recall  f1-score   support

         Bad       0.86      0.96      0.91      1085
        Good       0.98      0.90      0.94      1679

    accuracy                           0.93      2764
    macro avg       0.92      0.93      0.92      2764
    weighted avg       0.93      0.93      0.93      2764

### RANDOM FOREST
* Training Accuracy : 0.9317249698431845
* Testing Accuracy : 0.9337916063675832

**CLASSIFICATION REPORT**

              precision    recall  f1-score   support

         Bad       0.90      0.95      0.92      1147
        Good       0.96      0.92      0.94      1617

    accuracy                           0.93      2764
    macro avg       0.93      0.94      0.93      2764
    weighted avg       0.94      0.93      0.93      2764



 [-1]
 
THIS WEBSITE IS A PHISHING WEBSITE.
******************************

[1]

THIS WEBSITE IS A LEGITIMATE WEBSITE.





