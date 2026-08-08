# DevOps 3-Tier Exam App

A 3-tier DevOps mock exam application demonstrating a CI/CD pipeline with 
automated build, test, and code-quality checks using Jenkins, Docker, and 
SonarQube.

## Architecture
- **Frontend**: [brief note on what it is]
- **Backend**: [brief note on what it is]
- **Database**: [brief note - e.g. MySQL/Postgres]

## Pipeline
The Jenkinsfile automates:
1. Build stage — containerizes the app with Docker
2. Test/quality stage — runs SonarQube static analysis
3. Deploy stage — [describe if applicable]

## Setup
```bash
docker-compose up --build
```

## Reference
Built while following [KastroVKiran's DevOps project walkthrough](https://github.com/KastroVKiran) 
to learn end-to-end CI/CD pipeline design with Jenkins, Docker, and SonarQube.
