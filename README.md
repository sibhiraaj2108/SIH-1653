# Smart India Hackathon Workshop
# Date:
## Register Number:
## Name:
## Problem Title
SIH 1653: Web based Selector-Applicant Simulation Software
## Problem Description
Background: Recruitment and Assessment Centre (RAC) under DRDO, Ministry of Defence carries out interviews for applications received against advertised vacancies and for promotion to next higher grade for scientific manpower inducted within DRDO. Description: The process of interviewing is a challenging task. An unbiased objective interviewing process helps identify the right talent. The basic process of an interview involves posing a set of questions by an interviewer and thereafter evaluating responses from candidates. Thus, the questions asked should be relevant and match the area/ expertise of the applicant and the responses should also be of relevance w.r.t. the question asked. Expected Solution: The proposed solution should provide experts as well as candidates a real life Board Room experience, starting with initial ice-breaking questions leading to in-depth techno-managerial (depending on the level of candidate) questions. It shall also be able to provide a quantifiable score for experts as well as the candidate for the relevancy of questions w.r.t. the area/ expertise of the applicant. Similarly, candidate responses should also be graded for relevancy w.r.t. the question asked, finally assisting in arriving at an overall score for the subject knowledge of the candidate and thus his/ her suitability against the advertised post.

## Problem Creater's Organization
Ministry of Defence

## Idea
To develop a web-based simulation platform that provides a realistic interview environment for both selectors and applicants. This system should:
Enable structured interview flows starting from ice-breaking to in-depth domain questions.
Support intelligent matching of questions based on applicant profiles.
Allow real-time evaluation of both questions (for relevance) and responses (for correctness and depth).
Use NLP and AI models to quantify response relevance.
Generate automated interview reports and overall candidate fitment score.

## Proposed Solution / Architecture Diagram
                   ┌─────────────────────────────┐
                   │  Applicant Registration UI  │
                   └────────────┬────────────────┘
                                │
                   ┌────────────▼────────────┐
                   │ Profile Matching Engine │◄───┐
                   └────────────┬────────────┘    │
                                │                 │
                                ▼                 │
     ┌────────────┐   ┌──────────────────────┐    │
     │ Interview  │──►│  Question Generator   │◄───┘
     │ Simulator  │   └──────────────────────┘
     └────┬───────┘            │
          │                   ▼
          ▼         ┌──────────────────────┐
    ┌──────────┐    │ Candidate Response   │
    │ Expert UI│    │ Evaluation (AI/NLP)  │
    └────┬─────┘    └──────────┬───────────┘
         │                    ▼
         ▼           ┌──────────────────────┐
         └──────────►│ Scoring & Analytics  │
                     └──────────┬───────────┘
                                ▼
                      ┌──────────────────────┐
                      │ Result & Reporting   │
                      └──────────────────────┘
## Use Cases
Admin/HR Panel
Upload or manage job profiles
Set evaluation criteria
Monitor interview sessions
Expert/Interviewer Panel
View applicant profile and resume
Ask AI-suggested or custom questions
Evaluate candidate responses (manual + auto)
Candidate Panel
Login and attend simulated interview
Answer questions via text or video
Receive feedback post-interview
AI Components
Question Relevance Scorer: Rates how appropriate a question is to the candidate's profile
Response Grader: Uses NLP to evaluate how well the candidate answered
Final Score Aggregator: Combines all scores to suggest suitability

## Technology Stack
Component	Technology Used
Frontend (Web UI)	React.js / Angular
Backend API	Node.js / Python Flask / Django
Database	PostgreSQL / MongoDB
Authentication	JWT / OAuth 2.0
AI/NLP Models	OpenAI GPT / BERT / spaCy / Transformers
Video/Voice Integration	WebRTC / Twilio
Scoring & Analytics	Pandas + Plotly / D3.js
Deployment	Docker + Kubernetes + AWS/GCP/Azure

## Dependencies
AI/ML Libraries:
transformers, spaCy, nltk, scikit-learn for NLP and evaluation.
Frontend Libraries:
Material UI, TailwindCSS, Bootstrap.
Middleware/APIs:
Resume Parsing APIs, Text-to-Speech APIs (optional).
Third-party Integrations:
Twilio/WebRTC for video interviews
Resume parsers (like Affinda, Sovren)
