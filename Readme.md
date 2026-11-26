
# 🚨 RAGWatch
### A Cloud-Native Framework for Silent Regression Detection in Hybrid RAG Pipelines

<p align="center">
  <strong>Monitor. Evaluate. Detect. Protect.</strong>
</p>

<p align="center">
  <img src="https://img.shields.io/badge/Cloud-AWS-orange?style=for-the-badge&logo=amazonaws" />
  <img src="https://img.shields.io/badge/AI-RAG-blue?style=for-the-badge" />
  <img src="https://img.shields.io/badge/LLM-Ollama-black?style=for-the-badge" />
  <img src="https://img.shields.io/badge/Architecture-Serverless-green?style=for-the-badge" />
  <img src="https://img.shields.io/badge/Project-Academic-purple?style=for-the-badge" />
</p>

---

## 👥 Project Team

### Team Members

| S. No. | Name | Student ID |
|---|---|---|
| 1 | Yaswath | 2520030259 |
| 2 | Akilesh | 2520030570 |
| 3 | Bharath | 2520030169 |

### 👩‍🏫 Faculty Guide

**Dr. Harika Devi**  
Department of Computer Science and Engineering (CSE)

---

### 🎓 Course Information

| Detail | Information |
|---|---|
| Course Name | Cloud Infrastructure and Services |
| Course Code | 25CS2206E |
| Academic Year | 2026–2027 |
| Team Number | 22 |
| Section | 01 |
| Institution | CSE |
---
## 📌 Overview

**RAGWatch** is a cloud-native monitoring framework designed to detect silent regressions in Retrieval-Augmented Generation (RAG) pipelines.

Traditional monitoring systems focus primarily on infrastructure-level metrics such as CPU utilization, memory consumption, latency, and availability. However, these metrics cannot determine whether an AI system is retrieving the correct information or generating accurate, relevant, and reliable responses.

RAGWatch addresses this challenge by continuously evaluating RAG pipeline performance using a predefined **Golden Question Set**, quality evaluation metrics, retrieval analysis, token usage monitoring, and controlled fault injection.

The framework integrates a locally hosted Large Language Model (LLM) using **Ollama** with an **AWS serverless control plane**, enabling scalable, cost-efficient, and automated monitoring of AI systems.

---

## 🎯 Problem Statement

RAG systems can experience performance degradation without generating infrastructure alerts.

A pipeline may remain operational while:

- Retrieval quality silently decreases.
- Relevant documents are no longer retrieved.
- AI-generated responses become less accurate.
- Context relevance deteriorates.
- Latency increases.
- Token consumption and inference costs rise.
- Changes to components introduce unexpected failures.

Traditional infrastructure monitoring is insufficient to detect these AI-specific performance regressions.

### 💡 Our Solution

RAGWatch introduces an evaluation-driven monitoring framework that continuously measures the quality and operational performance of RAG pipelines and identifies potential regressions through baseline comparisons and automated monitoring workflows.

---

## 🚀 Key Features

- 🧪 **Golden Question Set Evaluation** – Evaluates the pipeline against a predefined collection of benchmark questions.
- 📊 **Quality Monitoring** – Tracks response quality and performance changes.
- 🔍 **Retrieval Monitoring** – Evaluates retrieval effectiveness and relevant context availability.
- ⚡ **Latency Monitoring** – Tracks execution and response latency.
- 💰 **Token Usage Monitoring** – Tracks token consumption and associated inference costs.
- 🧨 **Controlled Fault Injection** – Simulates pipeline degradation and failure conditions.
- 📉 **Regression Detection** – Identifies deviations from baseline evaluation results.
- ☁️ **Cloud-Native Architecture** – Uses AWS serverless services for monitoring workflows.
- 🤖 **Local LLM Integration** – Uses Ollama for locally hosted LLM inference.
- 📦 **Evaluation Artifact Storage** – Stores datasets, reports, and monitoring results.
- 🔐 **Secure Cloud Access** – Uses AWS IAM for access management.

---

## 🏗️ System Architecture

RAGWatch combines local AI inference and an AWS serverless monitoring infrastructure.

### Architecture Components

| Component | Technology | Purpose |
|---|---|---|
| AI Inference Engine | Ollama | Runs the locally hosted LLM |
| Evaluation Dataset | Golden Question Set | Provides benchmark queries |
| Object Storage | Amazon S3 | Stores datasets, reports, and artifacts |
| Serverless Compute | AWS Lambda | Executes monitoring and evaluation workflows |
| Monitoring | Amazon CloudWatch | Monitors logs, metrics, and execution performance |
| Database | Amazon DynamoDB | Stores evaluation results and regression records |
| Security | AWS IAM | Controls permissions and secure access |
| API Layer | Amazon API Gateway | Exposes monitoring and evaluation endpoints |

---

## 🔄 System Workflow

1. **Benchmark Initialization**  
   Load the predefined Golden Question Set.

2. **RAG Pipeline Execution**  
   Execute benchmark queries against the RAG pipeline.

3. **AI Response Generation**  
   Generate responses using the locally hosted LLM through Ollama.

4. **Evaluation and Metric Collection**  
   Measure response quality, retrieval effectiveness, latency, and token usage.

5. **Baseline Comparison**  
   Compare current evaluation results with baseline performance.

6. **Regression Analysis**  
   Identify possible quality or performance degradation.

7. **Cloud Processing**  
   AWS Lambda executes the monitoring and evaluation workflows.

8. **Data Storage**  
   Store evaluation records and monitoring artifacts using DynamoDB and S3.

9. **Monitoring and Logging**  
   CloudWatch captures operational logs and metrics.

10. **API Access**  
    API Gateway provides endpoints for accessing monitoring workflows.

---

## ☁️ AWS Services Used

| AWS Service | Purpose |
|---|---|
| 🪣 Amazon S3 | Stores evaluation datasets, reports, and monitoring artifacts |
| ⚙️ AWS Lambda | Executes serverless monitoring and evaluation workflows |
| 📈 Amazon CloudWatch | Monitors logs, metrics, and system performance |
| 🗄️ Amazon DynamoDB | Stores evaluation results, monitoring records, and regression information |
| 🔐 AWS IAM | Manages permissions and secure access to AWS resources |
| 🌐 Amazon API Gateway | Provides endpoints for accessing monitoring and evaluation services |

---

## 🧪 Evaluation Strategy

RAGWatch uses a predefined Golden Question Set to evaluate the behavior of a RAG pipeline under different conditions.

### Evaluation Dimensions

| Metric | Description |
|---|---|
| Response Quality | Measures the quality and correctness of generated responses |
| Retrieval Effectiveness | Measures whether relevant information is retrieved |
| Latency | Measures response and execution time |
| Token Usage | Tracks the number of tokens consumed |
| Cost Analysis | Estimates inference costs where applicable |
| Regression Status | Identifies deviations from the established baseline |

### Baseline-Based Monitoring

RAGWatch establishes a baseline evaluation profile for the RAG pipeline.

Subsequent evaluation runs are compared against this baseline to identify possible changes in performance.

The framework aims to identify regressions that may not be visible through conventional infrastructure monitoring.

---

## 🧨 Controlled Fault Injection

RAGWatch supports controlled fault injection to test its regression detection capabilities.

Fault injection allows the team to intentionally introduce controlled changes or degradation into the evaluation environment.

Potential experimental scenarios include:

- Retrieval quality degradation
- Changes in retrieval configuration
- Increased response latency
- Context quality degradation
- Changes in model behavior
- Token consumption changes

These experiments help evaluate whether the monitoring framework can identify meaningful performance changes.

---

## 📂 Project Structure

```text
RAGWatch/
│
├── README.md
├── docs/
│   ├── architecture/
│   ├── diagrams/
│   └── project-documentation/
│
├── datasets/
│   └── golden-question-set/
│
├── evaluation/
│   ├── baseline/
│   ├── results/
│   └── fault-injection/
│
├── monitoring/
│   ├── metrics/
│   └── regression-detection/
│
├── aws/
│   ├── lambda/
│   ├── api-gateway/
│   ├── dynamodb/
│   ├── s3/
│   └── iam/
│
├── scripts/
│
└── reports/
```

> The directory structure above represents a proposed organizational structure and can be updated to match the actual implementation.

---

## 🛠️ Technology Stack

### Artificial Intelligence
- Large Language Models (LLMs)
- Retrieval-Augmented Generation (RAG)
- Ollama
- Golden Question Set Evaluation

### Cloud Infrastructure
- Amazon Web Services (AWS)
- AWS Lambda
- Amazon S3
- Amazon DynamoDB
- Amazon CloudWatch
- AWS IAM
- Amazon API Gateway

### Development
- Python
- Git
- GitHub
- Cloud-native architecture
- Serverless computing

---

## 📈 Expected Outcomes

RAGWatch aims to:

- Detect silent quality regressions in RAG pipelines.
- Monitor AI performance beyond infrastructure metrics.
- Identify retrieval degradation.
- Track latency and token usage.
- Support controlled experimental evaluation.
- Improve the reliability of AI applications.
- Provide a scalable and cost-efficient monitoring framework.
- Support more trustworthy AI system deployment.

---

## 🔮 Future Scope

- Interactive monitoring dashboard.
- Automated regression alerts.
- Advanced RAG evaluation metrics.
- Multi-model evaluation support.
- Historical performance analytics.
- Automated threshold-based anomaly detection.
- CI/CD integration for RAG evaluation.
- Automated monitoring report generation.
- Support for multiple RAG architectures.
- Production-oriented observability integrations.

---

## 👨‍💻 Team

**Course:** Cloud Infrastructure and Services  
**Course Code:** 25CS2206E

| Team Member | Student ID |
|---|---|
| Yaswath | 2520030259 |
| Akilesh | 2520030570 |
| Bharath | 2520030169 |

**Team Number:** 22  
**Section:** 01

**Project Guide:** Dr. Harika Devi

---

## 🎓 Academic Project

This project is developed as part of the academic coursework for **Cloud Infrastructure and Services (25CS2206E)**.

The project demonstrates the integration of AI monitoring concepts, cloud-native infrastructure, serverless computing, evaluation methodologies, and performance regression detection.

---

## ⭐ Why RAGWatch?

> Infrastructure monitoring tells us whether a system is running. RAGWatch aims to help determine whether the AI system is still performing as expected.

RAGWatch bridges the gap between conventional cloud monitoring and AI-specific performance monitoring by combining benchmark-driven evaluation, baseline comparison, controlled experimentation, and cloud-native monitoring infrastructure.

---

<p align="center">
  <strong>RAGWatch — Watch Your RAG Before It Regresses.</strong>
</p>
