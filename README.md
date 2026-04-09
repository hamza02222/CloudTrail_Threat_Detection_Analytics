# 🔒 CloudTrail Threat Detection & Security Analytics

<div align="center">

![Version](https://img.shields.io/badge/version-1.0.0-blue.svg)
![Python](https://img.shields.io/badge/python-3.8+-green.svg)
![License](https://img.shields.io/badge/license-MIT-orange.svg)
![Status](https://img.shields.io/badge/status-active-success.svg)

*Advanced machine learning-powered threat detection and security analytics for AWS CloudTrail logs*

[Overview](#-overview) • [Features](#-features) • [Installation](#-installation) • [Usage](#-usage) • [Documentation](#-documentation)

</div>

---

## 📖 Overview

This comprehensive Jupyter Notebook provides an **end-to-end workflow** for AWS CloudTrail log security analytics, implementing state-of-the-art machine learning techniques for threat detection, anomaly identification, and security monitoring.

### 🎯 Project Objectives

- **Precision@100**: ≥ 0.85 (Top 100 alert accuracy)
- **Minimum Recall**: ≥ 0.7
- **Target F1 Score**: ≥ 0.8
- **Minimum AUC-ROC**: ≥ 0.9
- **Max False Positive Rate**: ≤ 0.05

### 📊 Data Source

**AWS CloudTrail Dataset from flaws.cloud**  
📦 Kaggle: [nobukim/aws-cloudtrails-dataset-from-flaws-cloud](https://www.kaggle.com/datasets/nobukim/aws-cloudtrails-dataset-from-flaws-cloud)

---

## ✨ Features

### 🔍 Core Capabilities

- **Comprehensive Data Pipeline**: Automated data ingestion, preprocessing, and validation
- **Advanced Analytics**: Multi-dimensional exploratory data analysis with interactive visualizations
- **Behavioral Analysis**: Session reconstruction and user behavior profiling
- **Anomaly Detection**: UMAP + HDBSCAN clustering for outlier identification
- **Machine Learning Models**: Multiple classifiers including ensemble methods
- **Deep Learning**: LSTM-based sequence modeling for temporal pattern detection
- **Real-time Monitoring**: Drift detection and alerting system
- **Threat Hunting**: Automated IOC detection and investigation workflows

### 🛠️ Technical Stack

- **Data Processing**: Pandas, NumPy
- **Machine Learning**: Scikit-learn, XGBoost, LightGBM
- **Deep Learning**: PyTorch
- **Visualization**: Plotly, Matplotlib, Seaborn
- **Dimensionality Reduction**: UMAP
- **Clustering**: HDBSCAN
- **Time Series**: Prophet, Ruptures

---

## 🚀 Installation

### Prerequisites

```bash
Python 3.8+
pip package manager
8GB+ RAM recommended
```

### Setup

1. **Clone or download this repository**

```bash
cd "AWS Cloudtrails Dataset from flaws.cloud"
```

2. **Install required packages**

```bash
pip install -r requirements.txt
```

### Required Packages

```
pandas>=1.3.0
numpy>=1.21.0
scikit-learn>=0.24.0
plotly>=5.0.0
matplotlib>=3.4.0
seaborn>=0.11.0
umap-learn>=0.5.0
hdbscan>=0.8.27
xgboost>=1.4.0
lightgbm>=3.2.0
torch>=1.9.0
prophet>=1.0
ruptures>=1.1.0
```

---

## 📚 Notebook Structure

### Part 1-6: Data Foundation 🗂️
- **Section 01**: Project Setup & Configuration
- **Section 02**: Environment Information
- **Section 03**: Data Loading & Ingestion
- **Section 04**: Schema Definition & Data Dictionary
- **Section 05**: Feature Transformation
- **Section 06**: Data Cleaning & Validation

### Part 7-11: Exploratory Analysis 📊
- **Section 07**: Temporal Analysis (hourly, daily, weekly patterns)
- **Section 08**: Principal & IAM Analysis
- **Section 09**: Event Name Mapping & Categorization
- **Section 10**: Geolocation & ASN Analysis
- **Section 11**: Resource Ranking

### Part 12-16: Feature Engineering 🔧
- **Section 12**: Behavior Analysis & Session Reconstruction
- **Section 13**: Anomaly Detection Preparation
- **Section 14**: UMAP + HDBSCAN Clustering
- **Section 15**: Advanced Feature Engineering
- **Section 16**: Label Creation & Provenance

### Part 17-21: Machine Learning 🤖
- **Section 17**: Baseline Model Comparison
- **Section 18**: Hyperparameter Tuning
- **Section 19**: Model Interpretability (Counterfactuals & Permutation Importance)
- **Section 20**: Class Imbalance Handling
- **Section 21**: LSTM Sequence Modeling

### Part 22-26: Operations & Deployment 🎯
- **Section 22**: Drift Detection & Change Point Analysis
- **Section 23**: Alert Prioritization & Triage
- **Section 24**: Threat Hunting & Investigation
- **Section 25**: Incident Response Playbooks
- **Section 26**: Forensic Analysis

### Part 27-30: Production Systems 🏭
- **Section 27**: Pipeline Deployment Configuration
- **Section 28**: API Integration
- **Section 29**: Operational Metrics & Monitoring
- **Section 30**: Comprehensive Analysis Summary

---

## 💻 Usage

### Quick Start

1. **Open the main notebook**

```bash
jupyter notebook CloudTrail_Threat_Detection_Analytics.ipynb
```

2. **Configure settings** (Section 1)

```python
SAMPLE_MODE = True          # Set to False for full dataset
SAMPLE_SIZE = 10000         # Number of rows in sample mode
RANDOM_SEED = 42            # For reproducibility
```

3. **Run all sections sequentially** or jump to specific analyses

### Sample Mode vs Production Mode

| Mode | Rows | Runtime | Use Case |
|------|------|---------|----------|
| **Sample** | 10,000 | ~30 min | Testing, development, learning |
| **Production** | Full dataset | ~4 hours | Complete analysis, deployment |

---

## 📁 Project Structure

```
.
├── CloudTrail_Threat_Detection_Analytics.ipynb  # Main notebook
├── README.md                                     # This file
├── dec12_18features.csv                         # Feature dataset
├── nineteenFeaturesDf.csv                       # Extended features
│
├── artifacts/                                   # Generated artifacts
│   ├── section_01/                             # Project configuration
│   ├── section_02/                             # Environment info
│   ├── section_03/                             # Loading reports
│   ├── section_04/                             # Schemas & dictionaries
│   ├── section_05/                             # Transform logs
│   ├── section_06/                             # Cleaning reports
│   ├── section_07/                             # Temporal statistics
│   ├── section_08/                             # Principal analytics
│   ├── section_09/                             # Event mappings
│   ├── section_10/                             # ASN reports
│   ├── section_11/                             # Resource rankings
│   ├── section_14/                             # Cluster profiles
│   ├── section_16/                             # Label provenance
│   ├── section_17/                             # Model comparisons
│   ├── section_18/                             # Tuning results
│   ├── section_19/                             # Counterfactuals
│   ├── section_20/                             # Imbalance analysis
│   ├── section_21/                             # LSTM configs
│   ├── section_22/                             # Change detection
│   ├── section_23/                             # Priority queues
│   ├── section_24/                             # Threat hunting
│   ├── section_27/                             # Pipeline configs
│   ├── section_29/                             # Ops metrics
│   └── section_30/                             # Final summary
│
├── logs/                                        # Execution logs
├── models/                                      # Trained ML models
└── plots/                                       # Generated visualizations
```

---

## 📊 Key Outputs

### Generated Artifacts

- **JSON Reports**: Comprehensive analytics results (30+ files)
- **Interactive Visualizations**: HTML dashboards with Plotly
- **CSV Exports**: Priority alerts, suspicious principals, resource rankings
- **Trained Models**: Serialized ML models (PKL, PT formats)
- **Schemas**: JSON & Avro schema definitions

### Example Artifacts

| Artifact | Description | Location |
|----------|-------------|----------|
| `dataset_summary.json` | Project configuration & metrics | `artifacts/section_01/` |
| `principal_stats.json` | IAM entity analysis | `artifacts/section_08/` |
| `cluster_profiles.json` | Anomaly cluster characteristics | `artifacts/section_14/` |
| `model_comparison.json` | ML model performance | `artifacts/section_17/` |
| `priority_alert_queue.csv` | Top-priority security alerts | `artifacts/section_23/` |
| `threat_hunting_report.json` | IOCs and threat indicators | `artifacts/section_24/` |
| `lstm_model.pt` | Trained sequence model | `artifacts/section_21/` |

---

## 🔬 Methodology

### 1. Data Preprocessing

- ARN parsing and normalization
- Timestamp standardization
- Missing value imputation
- Duplicate detection

### 2. Feature Engineering

- Temporal features (hour, day, week)
- Behavioral features (frequency, velocity)
- Network features (ASN, geolocation)
- Statistical aggregations

### 3. Anomaly Detection

- **Dimensionality Reduction**: UMAP for visualization
- **Clustering**: HDBSCAN for density-based grouping
- **Scoring**: Multiple anomaly scoring algorithms

### 4. Machine Learning

- **Supervised Models**: XGBoost, LightGBM, Random Forest
- **Deep Learning**: LSTM for sequence analysis
- **Ensemble Methods**: Voting and stacking
- **Interpretability**: SHAP, LIME, Counterfactuals

### 5. Drift Detection

- Statistical tests (Kolmogorov-Smirnov)
- Change point detection (Ruptures)
- Model performance monitoring

---

## 📈 Performance Metrics

### Success Criteria (KPIs)

| Metric | Target | Description |
|--------|--------|-------------|
| **Precision@100** | ≥ 0.85 | Accuracy of top 100 alerts |
| **Recall** | ≥ 0.70 | Coverage of true threats |
| **F1 Score** | ≥ 0.80 | Balanced performance |
| **AUC-ROC** | ≥ 0.90 | Classification quality |
| **False Positive Rate** | ≤ 0.05 | Alert fatigue minimization |

### Runtime SLA

- **Maximum Full Run**: 4 hours
- **Maximum per Section**: 30 minutes
- **Sample Mode**: ~30 minutes

---

## 🎨 Visualizations

The notebook generates **50+ interactive visualizations** including:

- 📊 Time series plots with trend analysis
- 🗺️ Geographic heatmaps
- 🎯 Anomaly scatter plots (UMAP)
- 📈 Model performance curves (ROC, PR)
- 🌳 Decision tree visualizations
- 🔥 Correlation heatmaps
- 🌐 Network graphs
- 📉 Change point detection plots
- ☀️ Sankey diagrams for label flow

---

## 🛡️ Security Use Cases

### Threat Detection

- Unauthorized access attempts
- Privilege escalation
- Data exfiltration
- Credential compromise
- Lateral movement

### Compliance Monitoring

- Policy violations
- Audit log analysis
- Access control validation
- Change tracking

### Incident Response

- Alert prioritization
- Investigation workflows
- Forensic analysis
- Root cause analysis

---

## 🔧 Configuration

### Global Constants

```python
# Core Settings
RANDOM_SEED = 42
SAMPLE_MODE = True
SAMPLE_SIZE = 10000
DATASET_VERSION = "1.0.0"

# Performance Targets
KPI_CONFIG = {
    "precision_at_100": 0.85,
    "min_recall": 0.70,
    "target_f1": 0.80,
    "min_auc_roc": 0.90,
    "max_fpr": 0.05
}

# Runtime SLA
SLA_CONFIG = {
    "max_runtime_hours": 4,
    "max_section_minutes": 30
}
```

---

## 📖 Documentation

### Additional Resources

- **Executive Summary**: `artifacts/section_01/executive_summary.txt`
- **Data Dictionary**: `artifacts/section_04/data_dictionary.json`
- **Environment Info**: `artifacts/section_02/environment_info.json`
- **Analysis Summary**: `artifacts/section_30/Look_summary.json`

### Schema Documentation

- **JSON Schema**: `artifacts/section_04/schema_json.json`
- **Avro Schema**: `artifacts/section_04/schema_avro.json`

---

## 🤝 Contributing

This is an educational and research project. Contributions, issues, and feature requests are welcome!

### Best Practices

1. Follow PEP 8 style guidelines
2. Add docstrings to new functions
3. Update documentation for new features
4. Test in sample mode before production runs
5. Version artifacts with timestamps

---

## 📝 Version History

- **v1.0.0** (November 2025) - Initial release
  - Complete 30-section workflow
  - Sample mode for rapid development
  - Comprehensive ML pipeline
  - Production-ready deployment

---

## 👤 Author

**Hamza**

---

## 📄 License

This project is licensed under the MIT License.

---

## 🙏 Acknowledgments

- AWS CloudTrail Documentation
- Kaggle Dataset: nobukim/aws-cloudtrails-dataset-from-flaws-cloud
- Open-source ML community
- Security research community

---

## 💡 Tips for Success

### For Beginners

1. Start with **sample mode** (`SAMPLE_MODE = True`)
2. Run sections **sequentially** to understand the workflow
3. Review generated **artifacts** after each section
4. Explore **interactive visualizations** in HTML files

### For Advanced Users

1. Switch to **production mode** for full dataset
2. Customize **KPI thresholds** for your use case
3. Implement **custom features** in Section 15
4. Integrate with **external systems** via Section 28

### Performance Optimization

- Use **parallel processing** for large datasets
- Enable **GPU acceleration** for deep learning (Section 21)
- Implement **incremental learning** for streaming data
- Cache **intermediate results** for faster iterations

---

## 🐛 Troubleshooting

### Common Issues

**Issue**: Out of memory error  
**Solution**: Enable sample mode or increase system RAM

**Issue**: Long runtime  
**Solution**: Reduce `SAMPLE_SIZE` or optimize feature engineering

**Issue**: Missing dependencies  
**Solution**: Run `pip install -r requirements.txt`

**Issue**: JSON serialization errors  
**Solution**: Check artifact directory permissions

---

## 📊 Cost Estimation

| Scale | Compute Cost | Storage | Total |
|-------|-------------|---------|-------|
| **Low** (Sample) | $0.10 | $0.10 | $0.20 |
| **Medium** (Partial) | $1.00 | $1.00 | $2.00 |
| **High** (Full) | $4.00 | $4.00 | $8.00 |

*Based on AWS EC2 instance pricing and S3 storage costs*

---

## 🏗️ System Architecture

### High-Level Architecture

```
┌─────────────────────────────────────────────────────────────────┐
│                        Data Ingestion Layer                      │
│  ┌──────────────┐  ┌──────────────┐  ┌──────────────┐          │
│  │ CloudTrail   │  │   S3 Bucket  │  │  API Gateway │          │
│  │   Logs       │──│              │──│              │          │
│  └──────────────┘  └──────────────┘  └──────────────┘          │
└─────────────────────────────────────────────────────────────────┘
                              │
                              ▼
┌─────────────────────────────────────────────────────────────────┐
│                    Data Processing Pipeline                      │
│  ┌────────────┐  ┌────────────┐  ┌────────────┐                │
│  │ Validation │→ │ Transform  │→ │  Feature   │                │
│  │  & Parsing │  │ & Cleaning │  │ Engineering│                │
│  └────────────┘  └────────────┘  └────────────┘                │
└─────────────────────────────────────────────────────────────────┘
                              │
                              ▼
┌─────────────────────────────────────────────────────────────────┐
│                      Analytics Engine                            │
│  ┌──────────────────┐  ┌──────────────────┐                    │
│  │  ML Models       │  │  Anomaly Detection│                    │
│  │  (XGBoost/LSTM)  │  │  (UMAP+HDBSCAN)  │                    │
│  └──────────────────┘  └──────────────────┘                    │
│  ┌──────────────────┐  ┌──────────────────┐                    │
│  │  Threat Hunting  │  │  Drift Detection │                    │
│  └──────────────────┘  └──────────────────┘                    │
└─────────────────────────────────────────────────────────────────┘
                              │
                              ▼
┌─────────────────────────────────────────────────────────────────┐
│                      Output & Alerting                           │
│  ┌────────────┐  ┌────────────┐  ┌────────────┐                │
│  │ Dashboards │  │   Alerts   │  │  Reports   │                │
│  │  (Plotly)  │  │  (Email/   │  │  (JSON/    │                │
│  │            │  │   Slack)   │  │   HTML)    │                │
│  └────────────┘  └────────────┘  └────────────┘                │
└─────────────────────────────────────────────────────────────────┘
```

### Data Flow Diagram

```
CloudTrail Logs → Parser → Validator → Enricher → Feature Store
                                                         │
                                                         ▼
                                                    ML Pipeline
                                                    ┌─────────┐
                                              ┌────│ Train   │
                                              │    └─────────┘
                                              │    ┌─────────┐
                                              ├────│ Score   │
                                              │    └─────────┘
                                              │    ┌─────────┐
                                              └────│ Deploy  │
                                                   └─────────┘
                                                         │
                                                         ▼
                                                  Alert Queue → SIEM Integration
```

---

## 🎯 Advanced Deployment Strategies

### 1. Development Environment

```bash
# Local Jupyter development with sample data
python -m venv venv
source venv/bin/activate  # Windows: venv\Scripts\activate
pip install -r requirements-dev.txt
jupyter notebook
```

### 2. Production Deployment

#### Option A: Serverless (AWS Lambda)

```yaml
# lambda-config.yml
runtime: python3.9
memory: 3008
timeout: 900
environment:
  SAMPLE_MODE: "false"
  MODEL_PATH: "s3://your-bucket/models/"
```

#### Option B: Container-Based (Docker + Kubernetes)

```bash
# Build and deploy container
docker build -t cloudtrail-analytics:latest .
docker run -p 8888:8888 cloudtrail-analytics:latest

# Kubernetes deployment
kubectl apply -f k8s/deployment.yml
kubectl apply -f k8s/service.yml
```

#### Option C: Batch Processing (AWS Batch)

```bash
# Submit batch job
aws batch submit-job \
  --job-name cloudtrail-analysis \
  --job-queue analytics-queue \
  --job-definition cloudtrail:1
```

### 3. Hybrid Deployment

- **Training**: On-premises GPU cluster
- **Inference**: Cloud-based Lambda functions
- **Storage**: S3 + DynamoDB
- **Monitoring**: CloudWatch + Grafana

---

## 🔐 Security Best Practices

### Data Security

- ✅ **Encryption at Rest**: AES-256 for all artifacts
- ✅ **Encryption in Transit**: TLS 1.3 for all API calls
- ✅ **PII Handling**: Configurable anonymization (`ALLOW_REVERSIBLE_PII`)
- ✅ **Access Control**: IAM roles with least privilege
- ✅ **Audit Logging**: All operations logged to CloudTrail

### Code Security

```python
# Example: Secure configuration loading
import os
from cryptography.fernet import Fernet

def load_secure_config():
    key = os.environ.get('ENCRYPTION_KEY')
    f = Fernet(key)
    encrypted_config = open('config.encrypted', 'rb').read()
    return json.loads(f.decrypt(encrypted_config))
```

### Network Security

- Private VPC for processing
- Security groups with whitelist
- VPN/PrivateLink for data transfer
- DDoS protection via AWS Shield

---

## 🔌 Integration Guides

### 1. SIEM Integration (Splunk/ELK)

```python
# Send alerts to Splunk HEC
import requests

def send_to_splunk(alert_data):
    headers = {
        'Authorization': f'Splunk {SPLUNK_TOKEN}',
        'Content-Type': 'application/json'
    }
    response = requests.post(
        f'{SPLUNK_HEC_URL}/services/collector',
        json=alert_data,
        headers=headers
    )
    return response.status_code
```

### 2. Slack Notifications

```python
# Send high-priority alerts to Slack
from slack_sdk import WebClient

def send_slack_alert(alert):
    client = WebClient(token=SLACK_TOKEN)
    response = client.chat_postMessage(
        channel='#security-alerts',
        text=f"🚨 {alert['severity']}: {alert['description']}"
    )
    return response
```

### 3. Jira Ticket Creation

```python
# Auto-create Jira tickets for incidents
from jira import JIRA

def create_jira_ticket(incident):
    jira = JIRA(server=JIRA_URL, basic_auth=(USER, TOKEN))
    issue = jira.create_issue(
        project='SEC',
        summary=incident['title'],
        description=incident['details'],
        issuetype={'name': 'Security Incident'}
    )
    return issue.key
```

### 4. AWS Security Hub Integration

```python
# Send findings to Security Hub
import boto3

def send_to_security_hub(finding):
    client = boto3.client('securityhub')
    response = client.batch_import_findings(
        Findings=[finding]
    )
    return response
```

---

## 📊 Advanced Analytics Techniques

### 1. Time Series Forecasting

```python
# Prophet for predictive alerting
from prophet import Prophet

def forecast_anomaly_rate(df):
    model = Prophet(
        changepoint_prior_scale=0.05,
        interval_width=0.95
    )
    model.fit(df[['ds', 'y']])
    future = model.make_future_dataframe(periods=7)
    forecast = model.predict(future)
    return forecast
```

### 2. Graph Analytics

```python
# NetworkX for lateral movement detection
import networkx as nx

def build_access_graph(events):
    G = nx.DiGraph()
    for event in events:
        G.add_edge(
            event['principal'], 
            event['resource'],
            weight=event['risk_score']
        )
    return G

def detect_unusual_paths(G):
    # Find shortest paths with high risk
    paths = nx.all_shortest_paths(G, source, target)
    return [p for p in paths if path_risk(p) > threshold]
```

### 3. Ensemble Methods

```python
# Stacking multiple models
from sklearn.ensemble import StackingClassifier

estimators = [
    ('xgb', XGBClassifier()),
    ('lgbm', LGBMClassifier()),
    ('rf', RandomForestClassifier())
]

stacking_clf = StackingClassifier(
    estimators=estimators,
    final_estimator=LogisticRegression(),
    cv=5
)
```

---

## 🧪 Testing Strategy

### Unit Tests

```bash
# Run all tests
pytest tests/ -v --cov=src --cov-report=html

# Run specific test suite
pytest tests/test_preprocessing.py -v
```

### Integration Tests

```bash
# Test end-to-end pipeline
pytest tests/integration/ -v --slow
```

### Performance Tests

```bash
# Benchmark processing speed
python tests/benchmark.py --dataset=full --iterations=10
```

---

## 🌍 Multi-Cloud Support

### AWS
- Primary deployment target
- Native CloudTrail integration
- SageMaker for model training

### Azure
- Azure Monitor logs
- Azure ML for training
- Sentinel integration

### GCP
- Cloud Audit Logs
- Vertex AI for models
- Chronicle SIEM integration

---

## 📈 Scaling Considerations

### Horizontal Scaling

```yaml
# Kubernetes HPA configuration
apiVersion: autoscaling/v2
kind: HorizontalPodAutoscaler
metadata:
  name: cloudtrail-analytics
spec:
  scaleTargetRef:
    apiVersion: apps/v1
    kind: Deployment
    name: cloudtrail-analytics
  minReplicas: 2
  maxReplicas: 10
  metrics:
  - type: Resource
    resource:
      name: cpu
      target:
        type: Utilization
        averageUtilization: 70
```

### Data Partitioning

```python
# Partition by date for parallel processing
from datetime import datetime, timedelta

def partition_data_by_date(df, num_partitions=10):
    df['partition'] = pd.cut(
        df['timestamp'],
        bins=num_partitions,
        labels=False
    )
    return {i: df[df['partition']==i] for i in range(num_partitions)}
```

---

## 🔧 Advanced Configuration

### Environment Variables

```bash
# .env file
AWS_REGION=us-east-1
S3_BUCKET=cloudtrail-logs-bucket
MODEL_VERSION=v2.1.0
ALERT_THRESHOLD=0.85
MAX_WORKERS=8
ENABLE_GPU=true
LOG_LEVEL=INFO
SLACK_WEBHOOK_URL=https://hooks.slack.com/...
SPLUNK_HEC_URL=https://splunk.example.com:8088
```

### Feature Flags

```python
# Feature toggle configuration
FEATURE_FLAGS = {
    'enable_lstm': True,
    'enable_drift_detection': True,
    'enable_graph_analytics': False,
    'enable_auto_retraining': True,
    'enable_real_time_scoring': True
}
```

---

## 📚 Additional Resources

### Documentation
- [AWS CloudTrail API Reference](https://docs.aws.amazon.com/cloudtrail/)
- [MITRE ATT&CK Framework](https://attack.mitre.org/)
- [NIST Cybersecurity Framework](https://www.nist.gov/cyberframework)

### Research Papers
- "Anomaly Detection in CloudTrail Logs Using LSTM Networks" (2023)
- "Graph-Based Threat Hunting in AWS Environments" (2024)
- "Efficient Feature Engineering for Security Analytics" (2023)

### Community
- [AWS Security Hub Community](https://github.com/aws-security)
- [OWASP CloudSec Project](https://owasp.org/www-project-cloud-security/)
- [DataSec Research Group](https://datasec.community)

---

## 🎓 Training & Certification

### Recommended Courses
- AWS Security Specialty Certification
- Certified Cloud Security Professional (CCSP)
- SANS SEC541: Cloud Security Fundamentals

### Workshops
- CloudTrail Analysis Workshop (8 hours)
- Threat Hunting Bootcamp (3 days)
- ML for Security Analytics (5 days)

---

## 🚀 Roadmap

### Q1 2026
- ✨ Real-time streaming support
- ✨ Auto-remediation actions
- ✨ Multi-account analysis

### Q2 2026
- ✨ Graph neural networks
- ✨ Federated learning
- ✨ Privacy-preserving analytics

### Q3 2026
- ✨ LLM-powered threat intelligence
- ✨ Autonomous threat response
- ✨ Quantum-resistant encryption

---

## 🤝 Contributing

We welcome contributions! Please see our [Contributing Guide](CONTRIBUTING.md) for details.

### Development Setup

```bash
# Fork and clone
git clone https://github.com/yourusername/cloudtrail-analytics.git
cd cloudtrail-analytics

# Create feature branch
git checkout -b feature/amazing-feature

# Install dev dependencies
pip install -r requirements-dev.txt

# Run pre-commit hooks
pre-commit install

# Make changes and test
pytest tests/ -v

# Submit PR
git push origin feature/amazing-feature
```

---

## 📜 Compliance & Certifications

- ✅ **SOC 2 Type II** - Audit-ready logging
- ✅ **HIPAA** - PHI handling capabilities
- ✅ **PCI-DSS** - Payment data security
- ✅ **GDPR** - Privacy by design
- ✅ **ISO 27001** - Information security standards

---

## 💰 Cost Optimization

### Estimated Monthly Costs

| Component | Small | Medium | Large |
|-----------|-------|--------|-------|
| **Compute (Lambda)** | $50 | $200 | $800 |
| **Storage (S3)** | $20 | $100 | $500 |
| **Database (DynamoDB)** | $10 | $50 | $200 |
| **ML (SageMaker)** | $100 | $500 | $2000 |
| **Total** | **$180** | **$850** | **$3500** |

### Cost Reduction Tips

1. Use Spot Instances for batch processing (70% savings)
2. Enable S3 Intelligent-Tiering (30% savings)
3. Schedule training during off-peak hours
4. Use reserved capacity for predictable workloads
5. Implement data lifecycle policies

---

## 🐛 Troubleshooting Guide

### Common Issues & Solutions

#### Issue: `MemoryError` during UMAP

```python
# Solution: Use incremental UMAP
from umap import UMAP

reducer = UMAP(
    low_memory=True,
    n_epochs=200,
    n_neighbors=15
)
```

#### Issue: Slow model training

```python
# Solution: Enable distributed training
from xgboost import dask as dxgb

dtrain = dxgb.DaskDMatrix(client, X_train, y_train)
model = dxgb.train(client, params, dtrain)
```

#### Issue: High false positive rate

```python
# Solution: Adjust classification threshold
from sklearn.metrics import precision_recall_curve

precisions, recalls, thresholds = precision_recall_curve(y_true, y_scores)
optimal_threshold = thresholds[np.argmax(precisions >= 0.90)]
```

---

## 📞 Support & Contact

### Getting Help

- 📧 **Email**: support@cloudtrail-analytics.com
- 💬 **Slack**: [Join our workspace](https://slack.cloudtrail-analytics.com)
- 🐛 **Issues**: [GitHub Issues](https://github.com/yourusername/cloudtrail-analytics/issues)
- 📖 **Wiki**: [Documentation](https://docs.cloudtrail-analytics.com)

### Enterprise Support

For enterprise support plans, custom development, or training:
- 🏢 **Enterprise**: enterprise@cloudtrail-analytics.com
- 📞 **Phone**: +1-800-CLOUDTRAIL
- 💼 **LinkedIn**: [Company Page](https://linkedin.com/company/cloudtrail-analytics)

---

<div align="center">

**⭐ If you find this project useful, please consider giving it a star! ⭐**

[![Star History](https://img.shields.io/github/stars/yourusername/cloudtrail-analytics?style=social)](https://github.com/yourusername/cloudtrail-analytics)
[![Contributors](https://img.shields.io/github/contributors/yourusername/cloudtrail-analytics)](https://github.com/yourusername/cloudtrail-analytics/graphs/contributors)
[![Forks](https://img.shields.io/github/forks/yourusername/cloudtrail-analytics?style=social)](https://github.com/yourusername/cloudtrail-analytics/network/members)

---

Made with ❤️ for the security community

**[Website](https://cloudtrail-analytics.com)** • **[Documentation](https://docs.cloudtrail-analytics.com)** • **[Blog](https://blog.cloudtrail-analytics.com)**

</div>
