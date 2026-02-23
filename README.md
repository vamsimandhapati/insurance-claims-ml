# InsuranceClaims ML

ML-powered insurance claims processing automation with NLP document parsing, fraud scoring, Spring Boot microservices, and React workflow dashboard.

[![Java 17](https://img.shields.io/badge/Java-17-ED8B00?style=flat&logo=openjdk&logoColor=white)](https://www.oracle.com/java/)
[![Spring Boot 3.2](https://img.shields.io/badge/Spring--Boot-3.2-6DB33F?style=flat&logo=spring-boot&logoColor=white)](https://spring.io/projects/spring-boot)
[![Python](https://img.shields.io/badge/Python-3.11-3776AB?style=flat&logo=python&logoColor=white)](https://www.python.org/)
[![React 18](https://img.shields.io/badge/React-18-61DAFB?style=flat&logo=react&logoColor=black)](https://reactjs.org/)
[![AWS](https://img.shields.io/badge/AWS-Deployed-FF9900?style=flat&logo=amazon-aws&logoColor=white)](https://aws.amazon.com/)

## Overview

InsuranceClaims ML automates the end-to-end insurance claims lifecycle. It ingests PDF/scanned claim documents, uses NLP (SpaCy + OpenAI) for entity extraction, a trained ML model for fraud probability scoring, and routes claims through a configurable workflow managed by Spring Boot microservices and a React adjudicator dashboard.

## Key Features

- **Intelligent Document Ingestion**: Extracts claimant info, policy numbers, and damage assessments from unstructured PDFs using NLP.
- **Fraud Probability Scoring**: Gradient Boosting model trained on historical claims data flags high-risk submissions.
- **Automated Workflow Routing**: BPM-style claim routing (Auto-Approve / Manual Review / Investigate) based on ML scores.
- **Adjudicator Dashboard**: React UI for claim reviewers with annotation tools, audit trails, and SLA tracking.
- **Integration-Ready**: REST APIs designed for integration with Guidewire and Majesco platforms.

## Tech Stack

- **Backend**: Spring Boot 3.2, Java 17, Spring Batch (bulk processing).
- **ML/NLP**: Python FastAPI, SpaCy, Scikit-learn, OpenAI API.
- **Frontend**: React.js, AG-Grid (for claim tables), Tailwind CSS.
- **Database**: PostgreSQL, Amazon S3 (document storage).
- **Cloud**: AWS ECS, RDS, Textract (OCR), Docker.

## Project Structure

```text
├── claims-service/        # Spring Boot claims ingestion and workflow
├── ml-scoring-engine/     # Python/FastAPI NLP + fraud scoring
├── adjudicator-dashboard/ # React claims review UI
├── document-processor/    # PDF parsing and OCR integration
└── infrastructure/        # Terraform AWS deployment
```

## License

MIT License. See [LICENSE](LICENSE) for details.
