<h1>Lightweight Ensemble Anomaly Detection for Hijacked IoT Devices</h1>
<h2>Abstract</h2>
<p>The rapid growth of IoT devices has significantly increased the attack surface of modern networks, making them vulnerable to hijacking and malicious use. Traditional intrusion detection systems often struggle to detect subtle or zero-day anomalies due to their reliance on static signatures and high computational requirements. This project proposes a Lightweight Ensemble Anomaly Detection Model designed specifically for IoT environments to efficiently identify hijacked devices in real time. By combining multiple machine learning classifiers, such as <b>Random Forest and Decision Tree</b>, in an ensemble structure, the model aims to improve detection accuracy while maintaining a low resource consumption suitable for IoT hardware. The system will be evaluated using publicly available IoT datasets and benchmarked against single-model baselines using metrics like <b>ROC-AUC, F1, precision, accuracy and CV scores</b>. This approach will seek to provide a more flexible and energy-efficient solution for mitigating IoT-based security threats.</p>
<h2>Methodology</h2>
<h3>Dataset</h3>
<p>The model is trained on the CIC-IDS-2023 dataset which includes real-time attack data on IoT devices. Attack data includes DDoS, DoS, Recon, Web-based, Brute-force, Spoofing, and Mirai attacks. For the sake of computational resources and time, this model is trained on the first twenty files in this data set, resulting in a sample size of 2,356,866 with over a million rows. The dataset consists of 46 features.</p>
<h3>Data Preprocessing</h3>
<p>Raw data is checked for missing values, null values, incorrect formatting and duplicates. The first step is cleaning the data of these impurities and then applying light weight scaling to standardize the mean to zero and standard deviation to one. Then, the data is fed into the model in order to achieve optimal results and accuracy.</p>
<h3>Proposed Algorithms</h3>
<p>Two machine-learning models were used for detecting anomalies, including Decision Tree and Random Forest. Then, an ensemble voting classifier used hard voting to take the combined average of each model’s prediction for a more confident prediction. </p>
<h2>Workflow Diagram</h2>
<img width="875" height="675" alt="image" src="https://github.com/user-attachments/assets/3872b08c-86bc-4007-a7a4-58126068ca04" />
<h2>Success Metrics</h2>
<p>By combining multiple machine learning classifiers, such as Random Forest and Decision Tree, in an ensemble structure, the model aims to improve detection accuracy while maintaining a low resource consumption suitable for IoT hardware. The system will be evaluated using publicly available IoT datasets and benchmarked against single-model baselines using metrics like F1, detection accuracy, CV and ROC-AUC scores. This approach will seek to provide a more flexible and energy-efficient solution for mitigating IoT-based security threats.</p>
<h3>Ensemble Voting Classifier</h3>
<p>A confusion matrix was generated to show the number of true positive, true negative, false positive and false negative predictions. The dark blue color being concentrated on the central linear line indicates a high rate of correct predictions.</p>
<img width="1016" height="883" alt="image" src="https://github.com/user-attachments/assets/9fd96019-da67-4683-83d1-c4ae4ef5fcdc" />
<h3>Model Evaluation</h3>
<p>Random Forest</p>
<ul>
  <li>Accuracy: 98.1643%</li>
  <li>F1: 97.9544%</li>
  <li>ROC-AUC: 97.2780%</li>
  <li>CV: 97.2018%</li>
</ul>

<p>Decision Tree⭐(Best Model)</p>
<ul>
  <li>Accuracy: 98.9429%</li>
  <li>F1: 98.9264%</li>
  <li>ROC-AUC: 96.0992%</li>
  <li>CV: 98.9476%</li>
</ul>
<h2>Future Work</h2>
<p>In future work we plan to focus mainly on expanding the ensemble system by incorporating additional lightweight classifiers such as Naïve Bayes or K-Nearest Neighbors, then running more test runs on them to further improve the prediction diversity. Another potential direction that we may take is to integrate a feature selection method that can automatically remove less informative redundant features that are unnecessary, which could reduce the computation time and improve the model performance on the constrained IoT devices, thus making it run more smoothly and be less time-consuming. Also, testing the system on real IoT hardware like Raspberry Pi or ESP32 boards would provide a better insight into how it would perform in the real world in terms of resource consumption, latency, and energy usage.</p>
<h2>Conclusions</h2>
<p>In conclusion, the study demonstrates that the lightweight ensemble anomaly detection framework can effectively enhance IoT security while also maintaining low computational cost by already having the CIC-IDS-2023 dataset preprocessed and training both the decision tree and random forest models and combining them using hard voting. The system also achieved strong detection results across multiple metrics. The ensemble approach provides a more stable prediction and reduced misclassification errors compared to individual models. The result shows that lightweight ensembles are a practical solution for securing the IoT networks, which often suffer from limited processing power and memory. The method given provides a better balance between accuracy and efficiency, making it more suitable for real-time detection in resource-constrained environments. The work lays a foundation for more future improvements involving more additional models, optimized feature sets, and more deployment on physical IoT hardware.</p>
