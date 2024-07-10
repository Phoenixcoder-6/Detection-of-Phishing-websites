# Detection-of-Phishing-websites
Dynamic detection of phishing websites using Supervised Machine Learning Techniques.

Cybersecurity is the practice of protecting systems, networks, and programs from digital attacks. These cyberattacks are usually aimed at accessing, changing, or destroying sensitive information; extorting money from users via ransomware; or interrupting normal business processes. It is a type of social engineering attack wherein an attacker impersonates to be a trusted contact and sends the victim fake mails. Unaware of this, the victim opens the mail and clicks on the malicious link or opens the mailicious attachment. By doing so, attackers gain access to confidential information and account credentials. Our project aims at detecting phishing websites using supervised machine learning approach. We try to build our ML model by judging all possible features of a website that can be taken into account – mainly focusing on address bar-based features and domain-based features.

For this project “Dynamic Detection of Phishing Websites using Supervised Learning”, we have built our own website, which is a combination of phishing URLs and legitimate URLs. The dataset comprises of near about 1500 phishing URLs collected from https://www.phishtank.com/developer_info.php and about 500 legitimate URLs which are collected from https://www.unb.ca/cic/datasets/url-
2016.html and other various sources.

This is followed by the Data Pre-processing step, which involves performing several filtering operations on the raw data, such as, removing redundant rows, checking for missing values, etc.

Feature extraction is a process of dimensionality reduction by which an initial set of raw data is reduced to more manageable groups for processing. This project mainly deals with two broad feature categories for every website – address bar-based features and domain-based features.


The relevant address bar-based features for this project are discussed as following:

o Presence of URL Shortening Services - TinyURL is one of the such URL shortening services. When tinyURL shortens a long web address, it creates a link in the form of letters and numbers that look nothing like the original. A short link may in fact lead to a scam website or one loaded with spyware, viruses or inappropriate content.

o Presence of IP Address in Domain Name - If IP address is present instead of a domain name in the URL, further if the IP address is not recognized by the WHOIS database, then the user can almost be sure that it is a Phishing website. If IP address is present in domain name, then it is considered as Phishing, else Legitimate.

o Presence of Prefix Suffix - The “-“ symbol is rarely used in legitimate URLs. Phishers tend to add this symbol, i.e., prefix and suffix separated by “-“ symbol in the domain name, so that the users can feel free thinking that they are accessing a legitimate and true website.

o Length of URL - The proposed length of a legitimate URL is 75 characters or less. If the average length of URL taken from the dataset is more than 75 characters, then it is considered as Phishing, else Legitimate.

o Presence of Favicon – If the favicon (favourite icon) of a website is present, then it is considered as Legitimate, else Phishing.

The relevant domain-based features for this project are as following:

o Age of Domain - If the domain is registered for more than two years in the
WHOIS database, then it is considered as Legitimate, else Phishing.

o Presence of DNS Records – If the DNS records for a particular website do
not exist, then it is considered as Phishing, else Legitimate.

o Google Index – If the webpage displayed by the URL is indexed by Google,
then it is considered as Legitimate, else Phishing.

Different algorithms have been used for the efficient classification purpose, such as
Linear Support Vector Machine, Logistic Regression and Random Forest.

Approach:

Firstly, each classifier is implemented for each feature of a website – address bar-
based features and domain-based features. This is followed by implemented a
combination of several feature/s and implementing new classifiers one after another.
This is done with the objective of checking which features set proves to be more
important in predicting the legitimacy of a website. At every step of implementing
classifiers, it is highly important to take care of the model accuracy and model
performance – lower the cost and higher the model accuracy, better is the model for
machine learning tasks.

Mathematical Intuition


Total number of extracted features = 8
According to problem statement,

Total number of combinations = 8 C 1 + 8 C 2 + 8 C 3 + 8 C 4 + 8 C 5 + 8 C 6 + 8 C 7 + 8 C 8 = 8 + 28 + 56 + 70 + 56 + 28 + 8 + 1 = 255
This means that,

 When classifiers are implemented with a single feature each time, we obtain 8 such combinations.

 When classifiers are implemented with any two features at a time out of 8 features, we obtain 28 such combinations.

 When classifiers are implemented with any three features at a time out of 8features, we obtain 56 such combinations.

 When classifiers are implemented with any four features at a time out of 8features, we obtain 70 such combinations.

 When classifiers are implemented with any five features at a time out of 8 features,we obtain 56 such combinations.

 When classifiers are implemented with any six features at a time out of 8 features,we obtain 28 such combinations.

 When classifiers are implemented with any seven features at a time out of 8 features, we obtain 8 such combinations.

 And lastly, we obtain another combination which comprises of all 8 features.
