# Random Quote Generator (Serverless)

This project is a modern, serverless web application that generates random motivational quotes. The frontend is a single HTML page with embedded CSS and JavaScript, featuring a glassmorphism design, animated pop-ups, celebration particle effects, and dynamic gradient backgrounds.

The backend is implemented using AWS Lambda (Python) and accessed through Amazon API Gateway. Each time a user clicks the “Generate Quote” button, the frontend sends a request to the API Gateway, which triggers the Lambda function to select a random quote and return it to the dashboard.

## Services used and configurations:

- AWS Lambda: Configured with Python runtime to handle quote generation and API requests.

- API Gateway: Configured to expose a HTTP endpoint for the frontend to call, including CORS headers.

- Frontend: Single-page HTML with embedded CSS and JavaScript for styling, animations, and API integration.

- This setup demonstrates a small-scale serverless architecture with a functional, visually appealing frontend and a cloud-hosted backend API.

![Version](https://img.shields.io/badge/version-1.0.0-blue)
![AWS](https://img.shields.io/badge/AWS-Lambda%20%7C%20API%20Gateway%20%7C%20DynamoDB%20%7C%20S3-orange)

## Features

• Random motivational quote generator  
• Modern glass-style UI dashboard  
• Animated popup quote display  
• Celebration particle animation  
• Dynamic gradient background changes  
• Serverless cloud backend


## Tech Stack

Frontend
- HTML
- CSS
- JavaScript

Backend
- AWS Lambda (Python)

API Layer
- Amazon API Gateway

Cloud Platform
- Amazon Web Services


## System Architecture

User Browser  
↓  
Frontend Dashboard (HTML)  
↓  
API Gateway  
↓  
AWS Lambda Function  
↓  
Random Quote Response

![image alt](https://github.com/Arjun-Nalge/Random-Quote-Generator/blob/edceea3091e3d6d5367de3fba3efbaa82f0a5afb/archi-img.png)

## Author
Arjun Nalge - DevOps Engineer

[![LinkedIn](https://img.shields.io/badge/LinkedIn-Connect-blue?logo=linkedin)](https://www.linkedin.com/in/arjun-nalge-313642398)
[![GitHub](https://img.shields.io/badge/GitHub-Follow-black?logo=github)](https://github.com/Arjun-Nalge/Arjun-Nalge.git)

## 🏗️ System Flow

The application is hosted entirely on AWS, utilizing a 100% serverless stack to ensure high availability and cost-efficiency.

```mermaid
graph TD
    User((User)) -->|Access URL| S3[Amazon S3 Static Hosting]
    S3 -->|Serves| UI[Frontend Dashboard]
    UI -->|API Request| APIG[Amazon API Gateway]
    APIG -->|Trigger| Lambda[AWS Lambda - Python]
    
    subgraph "Data & Logic Layer"
    Lambda -->|Fetch/Log| DB[(Amazon DynamoDB)]
    Lambda -->|Process| Logic{Randomizer Engine}
    end

    Logic --> Lambda
    Lambda -->|JSON Response| APIG
    APIG -->|Display Quote| UI
    UI -->|Celebration Effect| User

    style S3 fill:#FF9900,stroke:#fff,color:#fff
    style Lambda fill:#FF9900,stroke:#fff,color:#fff
    style DB fill:#405B8C,stroke:#fff,color:#fff
    style APIG fill:#8C4FFF,stroke:#fff,color:#fff
