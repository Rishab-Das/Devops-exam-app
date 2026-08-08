# DevOps 3-Tier Exam App

A 3-tier DevOps mock exam application demonstrating a CI/CD pipeline with 
automated build, test, and code-quality checks using Jenkins, Docker, and 
SonarQube. The app itself is a quiz platform that tests DevOps knowledge 
(Jenkins, Maven, Tomcat, SonarQube, etc.) and generates a completion 
certificate as a PDF.

## Architecture
- **Frontend**: HTML/CSS templates (exam, results, admin dashboard) rendered 
  server-side by Flask
- **Backend**: Python Flask app serving quiz questions, handling sessions, 
  scoring, and PDF certificate generation (via xhtml2pdf)
- **Database**: MySQL — stores each participant's submission (username, 
  email, score, timestamp)

## Pipeline
The Jenkinsfile automates:
1. Build stage — builds the Docker image for the Flask app
2. Test/quality stage — runs SonarQube static analysis on the codebase
3. Deploy stage — spins up the app via docker-compose (Flask + MySQL)

## Setup
```bash
docker-compose up --build
```
The app will be available on the port defined in `docker-compose.yml`.

## Reference
Built while following [KastroVKiran's DevOps project walkthrough](https://github.com/KastroVKiran) 
to learn end-to-end CI/CD pipeline design with Jenkins, Docker, and SonarQube.
