Overview:
This assignment is built around three things — understanding a data mining topic in depth, applying it to a real dataset, and comparing it against a second technique. The topic here is DBSCAN clustering, which is used to detect anomalies in weekly sales transaction data. It is then compared directly against KMeans clustering to see how the two approaches differ in practice. 

Dataset:
The dataset is Sales_Transactions_Dataset_Weekly.csv, which contains weekly sales transaction records across multiple products.

How to Run It:
Make sure pandas, numpy, matplotlib, seaborn, and scikit-learn are installed, then run the Python script or open the notebook and execute all cells in order. The preprocessing, KMeans clustering, DBSCAN clustering, and comparison visualisations are all clearly labelled in the code.

Conclusion:
This analysis emphasizes the complementary roles of DBSCAN and KMeans in sales anomaly detection. DBSCAN is particularly well-suited for most operational scenarios, demonstrating high computational efficiency (0.0099 seconds training time) and strong detection performance (ROC AUC=0.9975, accuracy=0.9951). Despite some false positives (precision=0.2000), it reliably identifies all true anomalies (recall=1.0000) making it suitable for real-time monitoring. On the other hand, KMeans achieves perfect recall but has a significant false-positive ratio of 40:1 due to its spherical cluster assumption, making it viable only for high-risk situations where missing anomalies is unacceptable such as in fraud detection. The methods have distinct limitations that are worth noting: DBSCAN is less effective when faced with non-uniform data density distributions, while KMeans encounters significant challenges due to its assumption of spherical clusters, particularly in high-dimensional feature spaces. To conclude, DBSCAN provides an effective balance of speed and accuracy for sales analytics, while KMeans can serve as a complementary screening system. These findings offer valuable guidance for selecting anomaly detection methods tailored to specific business needs.
