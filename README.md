# AI-Powered Mobile (iOS) — Serverless Cloud Backend + Computer Vision

This graduation project is a smart mobile application that combines conversational AI, cloud computing, and computer vision to deliver a scalable and context-aware chatbot experience. Users can chat using text or voice, and the chatbot can enhance its replies using visual context from a computer vision module.

## Architecture
<img width="611" height="669" alt="Screenshot 2026-02-01 153046" src="https://github.com/user-attachments/assets/3963584b-03f8-4382-9fd2-d39dbaed441f" />


The system follows a modular design:
- **iOS app (Swift)** is the main user interface (text + voice).
- A **serverless backend on AWS** handles requests and generates chatbot responses.
- A **computer vision module (YOLO)** provides detection results that can be used as extra context.

## My Contribution (Primary) — Chatbot + Cloud Backend
My main responsibility in this project was the **chatbot system**, including its **AWS serverless backend** and its integration with the iOS client.

This includes:
- Designing the chatbot flow and response format
- Building the cloud API used by the mobile app
- Implementing request processing and orchestration in AWS Lambda
- Integrating Amazon Bedrock (LLM) for language understanding and response generation
- Handling session/state logic (when enabled)

## Team Collaboration — Chatbot ↔ YOLO Integration (Drowsiness Detection)
In collaboration with the team, the chatbot was integrated with a **YOLO-based drowsiness detection** module to enrich responses with visual context.

Integration flow:
- The YOLO module outputs structured results (e.g., **drowsiness status**, labels, and confidence scores)
- These results are sent to the chatbot as contextual input
- The chatbot interprets the vision signals and generates clear, human-friendly guidance and responses

## AWS Serverless Backend (Chatbot)
- **Amazon API Gateway** — secure entry point for mobile requests  
- **AWS Lambda** — core request processing and orchestration  
- **Amazon Bedrock (LLM)** — natural language understanding + response generation  
- **Optional services**
  - **DynamoDB** — session/state data (optional)
  - **S3** — logs/media storage (optional)

This architecture is designed for scalability, low operational overhead, and cost efficiency.

## Features
- Text and voice-based chatbot interaction
- Multilingual support (e.g., English / Arabic)
- Context-aware responses using an LLM
- Secure client ↔ backend communication (REST API)
- Vision-aware responses when detection context is provided

## Tech Stack
- **Mobile:** iOS (Swift), Speech-to-Text
- **Cloud (AWS):** API Gateway, Lambda, Bedrock, DynamoDB (optional), S3 (optional)
- **AI/CV:** LLMs, YOLO Drowsiness Detection
- **Architecture:** REST APIs, Serverless Computing

## Notes
This project is for educational and research purposes as part of a graduation project.
