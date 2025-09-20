## 🤖 Study Mate - Your AI Study Assistant

It is a sophisticated learning companion designed to streamline the process of understanding and engaging with educational materials. It leverages advanced AI capabilities to analyze documents, provide concise summaries, facilitate interactive Q&A sessions, and generate personalized quizzes. This tool aims to enhance learning efficiency and comprehension for students and researchers alike.

## Core Functionalities

- **PDF Analysis & Text Extraction**: The system can ingest PDF documents, extract their textual content, and prepare it for further AI processing.

- **Summarization**:  Generates both high-level "Quick Notes" and in-depth "Key Takeaways" from the extracted text, aiding in rapid comprehension and retention.

- **Interactive Chatbot**: Enables users to ask questions directly about the document content. The chatbot provides context-aware answers, fostering a deeper understanding of complex topics.

- **Quiz Generation**: Creates multiple-choice quizzes based on the document's content, allowing users to test their knowledge and identify areas for further study.

## Architecture Overview

1 **Frontend (Next.js)** 

- UI Components: Built with Shadcn UI components for a consistent and accessible user interface.
- State Management: React's useState and useRef hooks manage component-level state.
- API Integration: The lib/api module handles all communication with the backend API.
- Styling: Tailwind CSS is used for utility-first styling, with globals.css defining global styles and theme variables.

2 **Backend (FastAPI)**

- API Endpoints: Defined in routers/ for document handling, chat, and quiz generation.
- AI Services: Encapsulated in services/ to abstract AI model interactions (e.i., GeminiService).
- Data Models: Pydantic models in models/ define request and response structures.
- Configuration: config.py manages application settings, including API keys and CORS origins.


 3 **Deployment**: Used Render for deploying the FastApi backend and Vercel for the frontend, and then joined them using CORS

## Try the web APP 

🌐 Live : https://study-mate-murex.vercel.app 

## How to Use HealthAI locally 

1. **Clone the Repository**:

   ```bash
   git clone https://github.com/DRITI2906/Study-Mate.git
   cd Study-Mate
   ```

2. **Setup Backend**:

   ```bash
   cd backend
   # create .env file and add this things in it 
   # GEMINI_API_KEY=your_key
   # CORS_ORIGINS= (http://localhost:3000)
   # MODEL_NAME= (gemini-2.5-flash)
   python -m venv venv
   .\venv\Scripts\activate     
   pip install -r requirements.txt
   uvicorn main:app --reload 
   ```   

3. **Setup Frontend**:

   ```bash 
   npm run dev
   ```    

## ✨ Why Study Mate?

Traditional study methods make it difficult to quickly grasp key concepts, retain information, and stay engaged. Study Mate bridges this gap by acting as an AI-powered personal study companion that transforms the way you learn.

- **🚀 Save Time** – Instantly summarize long documents into quick notes & key takeaways(which are can be downloaded as well).
- **💡 Interactive Learning** – Ask questions and get context-aware AI answers.
- **📝 Personalized Quizzes** – Test knowledge with auto-generated quizzes(which are can be downloaded as well).
- **🎯 Focused Revision** – Highlight key concepts for better retention.
- **🌐 Seamless Experience** – Simple UI, PDF support, and cross-platform access.
- **🤖 AI-Powered** – Smart, adaptive, and designed to enhance learning efficiency.

## 📸 ScreenShots

![Upload page](<screenshots/upload.png>)
![Summary page](<screenshots/summary.png>)
## Chatbot
![Chatbot](<screenshots/chatbot.png>)
# Quiz
![Quiz page](<screenshots/quuiz.png>)

## Developers Information

Created by Driti Rathod. Connect with me on 

- [GitHub](https://github.com/DRITI2906)
- [LinkedIn](https://www.linkedin.com/in/driti-rathod-ab038a294/)
- [Email](mailto:dritirathod2906@gmail.com)