Creating a predictive analytics system for detecting phishing emails in real-time from a Zimbra email server with streaming data:

**1. Data Ingestion:**
   - **Component**: Apache Kafka
   - **Explanation**: Use Apache Kafka to ingest email data streams from the Zimbra email server. Kafka provides reliable and scalable message streaming.

**2. Data Preprocessing:**
   - **Component**: Apache Spark Streaming
   - **Explanation**: Apache Spark Streaming can preprocess the incoming email data in real-time. You can use Spark's DataFrames and MLlib for feature extraction and initial data cleaning.

**3. Feature Extraction:**
   - **Component**: Apache NLP Libraries (e.g., NLTK, spaCy)
   - **Explanation**: Utilize natural language processing (NLP) libraries to extract relevant features from email text, such as keywords, email structure, and sentiment analysis.

**4. Machine Learning Model:**
   - **Component**: Scikit-Learn, TensorFlow, or PyTorch
   - **Explanation**: Train and deploy machine learning models (e.g., Random Forest, Neural Networks) to classify emails as phishing or legitimate. Continuously update the model using streaming data.

**5. Real-time Scoring:**
   - **Component**: Apache Flink or Apache Storm
   - **Explanation**: Apache Flink or Apache Storm can score incoming emails using the trained machine learning model in real-time.

**6. User Alerts and Actions:**
   - **Component**: Email Notification System (e.g., SMTP)
   - **Explanation**: Implement a system to send alerts to users or administrators when a phishing email is detected. Actions may include flagging the email, quarantining it, or blocking malicious URLs.

**7. Feedback Loop:**
   - **Component**: Elasticsearch and Kibana
   - **Explanation**: Use Elasticsearch to store logs and Kibana for real-time monitoring and analysis of system performance and detected threats. Create dashboards to visualize the effectiveness of the phishing detection system.

**8. Model Version Control:**
   - **Component**: Git or a dedicated model version control system
   - **Explanation**: Keep track of different versions of your machine learning models to facilitate easy rollback or updates.

**9. Scalability and High Availability:**
   - **Component**: Kubernetes or Docker Swarm
   - **Explanation**: Use container orchestration tools like Kubernetes or Docker Swarm to manage the scalability and high availability of your streaming analytics pipeline.

**10. Data Storage (Optional):**
   - **Component**: Apache Cassandra or Elasticsearch
   - **Explanation**: If you need to store and query historical data for analysis or compliance purposes, consider using a NoSQL database like Apache Cassandra or Elasticsearch.

**11. Continuous Integration/Continuous Deployment (CI/CD):**
   - **Component**: Jenkins or GitLab CI/CD
   - **Explanation**: Implement CI/CD pipelines to automate testing, deployment, and updates of your predictive analytics system.

**12. Data Privacy and Compliance:**
   - **Component**: Privacy-preserving techniques and compliance frameworks (e.g., GDPR, HIPAA)
   - **Explanation**: Ensure that your system complies with data privacy regulations and incorporates privacy-preserving techniques, especially when handling email data.

**13. Logging and Monitoring:**
   - **Component**: Prometheus and Grafana
   - **Explanation**: Set up logging and monitoring using Prometheus for metrics collection and Grafana for visualization to track system performance and detect anomalies.

**14. User Interface (Optional):**
   - **Component**: Django, Flask, or React
   - **Explanation**: Develop a user interface for administrators to configure the system, review alerts, and manage the phishing detection pipeline.

This architecture provides a comprehensive solution for predictive analytics on streaming email data from a Zimbra server.
It combines various open-source tools and frameworks to handle data ingestion, preprocessing, machine learning, real-time scoring, user alerts, and monitoring.
Keep in mind that this is a complex system, and it should be designed and implemented with careful consideration of security and privacy concerns.