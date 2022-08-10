# Detecting-Ransomware-using-Machine-Learning-Models

Ransomware is a type of sophisticated virus that uses encryption to prohibit users from accessing their data unless a ransom is paid to the attacker. The threat presented by ransomware is quite severe, with new varieties and families being discovered on the internet and dark web on a regular basis. The rise in ransomware is also accompanied by an increase in the usage of artificial intelligence. Machine learning and deep learning techniques to detecting ransomware are attracting a lot of attention since machine learning and deep learning can identify zero-day threats. Deep Neural Networks have been shown to function effectively with time series data, as well as multi-class classification and clustering issues, and they capture varying levels of granularity of the underlying structure in the data set at various layers of the model architecture.

Deep learning and machine learning have an impact on every part of life. Because of their decision-making capabilities, these technologies have a wide range of applications in every discipline. Deep learning is the most effective method for detecting the patterns of a working system. It has a wide range of applications because to its pattern recognition capabilities. Machine learning and deep learning are burgeoning technologies that are widely employed in advanced cybersecurity research. These technologies should also be applied to the detection of ransomware. In terms of pattern recognition, both systems were useful. Machine learning and deep learning are used to detect a variety of viruses and ransomware.

# Dataset

The implementation starts with the gathering of data from UCI BitcoinHeistRansomwareAddressDataset. It consists of  The dataset consists of 10 attributes anf the number of instances are 1048575. The features of the dataset are:

address: String. Bitcoin address.

year: Integer. Year.

day: Integer. Day of the year. 1 is the first day, 365 is the last day.

length: Integer.

weight: Float.

count: Integer.

looped: Integer.

neighbors: Integer.

income: Integer. Satoshi amount (1 bitcoin = 100 million satoshis).

label: Category String. Name of the ransomware family (e.g., Cryptxxx, cryptolocker etc) or white (i.e., not known to be ransomware).

# Implementation

1. Data collection

2.	The, comes the data pre-processing. Irrelevant features like year, day, Bitcoin address were dropped since year and day does not add any value to the classification and each of the Bitcoin addresses are unique so it’s of no use in the task of detecting bitcoin ransomware addresses.

3.	Binary label encoding was performed on target label, neighbours, length, count, looped columns. In target label column white label was encoded as 1 and rest of the labels grouped as black label was encoded as 0. In neighbour column those values which was greater than 2 was encoded 0 else 1, in length column those values which was greater than 8 was encoded as 0 else 1, in count as well as looped columns those values which was greater than 1 was encoded as 0 else 1. Encoding as 1 indicates it’s a non-ransomware address whereas encoding 0 indicates it’s a ransomware address.

4.	Model Building: The dataset was divided into 80% train and 20% test splits. Various scaling techniques like StandardScaler, MinMaxSccaler, RobustScaler was applied to both the train and test data to scale them down appropriately.

5.	After that, various supervised classification machine learning models was applied like logistic regression, KNN, SVM, Decision Tree, Random Forest, AdaBoost, XGBoost, Neural Networks. To evaluate our models, we have used metrics like accuracy, precision, recall, F1 score and ROC

•	True positive rate (T P R) = T P/ (T P + F N ……………... (1)

•	False positive rate (F P R) = F P/ (F P + T N) ……………. (2)

•	Precision = T P/ (T P + F P) ………………………………. (3)

•	Recall = T P/ (T P + F N) …………………………………. (4)

•	F-measure = 2∗Precision∗Recall/ (Precision + Recall) …… (5)

•	Accuracy = T P + T N/ (T P + T N + F P + F N) …………. (6)

# Applicability Category

Our project has a wide variety of applicability in many real-life categories and scenarios. It is relevant in the following areas:

1. Social Relevance: The number of ransomware variants has increased rapidly every year, and ransomware needs to be distinguished from the other types of malwares to protect users' machines from ransomware-based attacks. Ransomware detection, hence, shall act as a safeguard for the society to protect people’s sensitive information.

2. Healthcare: Ransomware is a type of malware that infects systems and files, rendering them inaccessible until a ransom is paid. When this occurs in the healthcare industry, critical processes are slowed or become completely inoperable. Hospitals are then forced to slow down the medical process and ultimately soaking up funds. Thus, the project shall prove beneficial there.

3. Social Networking: Online social networks (OSNs) have become the new vector for cybercrime, and hackers are finding new ways to propagate spam and malware on these platforms. Hence, Ransomware detection shall help in preventing this social malware.

# Conclusion

With the increased number of ransomware-based cyber-attacks, ransomware detection methods are needed. Even though ransomware share many aspects of features with other types of malware, some features are specific to ransomware. Because neural networks have the capacity to learn on their own and produce output which is not limited by inputs, they can learn from past events and apply what they have learned whenever a similar circumstance arises, enabling them to cope with real-time problems, therefore it performs better than conventional machine learning algorithms. The methodology identified in this project, is a robust strategy for detecting ransomware and can give more effective defenses against future ransomware assaults.
