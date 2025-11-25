
# 🎧 PrepWise – AI-Powered Mock Interview Simulator

PrepWise is an intelligent mock-interview simulator built using Vapi AI voice agents, Google Gemini, and Firebase. It helps users practice interviews through real-time voice conversations, follow-up questions, and detailed performance feedback.

## 🚀 Features

* 🔐 **Authentication:**
  Secure Sign Up and Sign In using Firebase Authentication with server-side session cookies.

* 🎙️ **Create Interviews:**
  Easily generate custom interview sessions by selecting:

  * Role
  * Interview type
  * Difficulty level
  * Tech stack
    
  Powered by Vapi Voice AI + Google Gemini.
  
* 🗣️ **Real-Time AI Interview:**
  Conduct a realistic voice-based interview with an AI agent. Includes:

  * Natural back-and-forth interaction
  * Live transcript generation

* 📊 **Smart Feedback Report:**
  After the interview, PrepWise generates a detailed performance summary using Google Gemini, covering:

  * Communication Skills
  * Technical Depth
  * Problem-Solving Ability
  * Cultural Fit
  * Confidence & Clarity

* 💻 **Modern & Clean UI:**
  Crafted with Next.js + Tailwind CSS + shadcn/ui for a smooth, minimal, and responsive design.

* 🧭 **Personal Dashboard:**
  Track your interview sessions, view transcripts, review feedback, and analyze your progress over time.

* 📱 **Fully Responsive:**
  Optimized for all devices — mobile, tablet, and desktop.

  
## 🛠️ Tech Stack

* **Next.js 14 (App Router)**
* **Firebase Auth & Firestore**
* **Tailwind CSS**
* **Vapi AI** (voice interviews)
* **Google Gemini** (AI feedback and analysis)
* **shadcn/ui** (beautiful, accessible components)

<p align="left">
  <img src="https://img.shields.io/badge/Next.js-000000?style=for-the-badge&logo=nextdotjs&logoColor=white" />
  <img src="https://img.shields.io/badge/Firebase-FFCA28?style=for-the-badge&logo=firebase&logoColor=black" />
  <img src="https://img.shields.io/badge/TailwindCSS-38B2AC?style=for-the-badge&logo=tailwindcss&logoColor=white" />
  <img src="https://img.shields.io/badge/Vapi_AI-6D3DF3?style=for-the-badge" />
  <img src="https://img.shields.io/badge/Google_Gemini-4285F4?style=for-the-badge&logo=google&logoColor=white" />
  <img src="https://img.shields.io/badge/shadcn/ui-000000?style=for-the-badge" />
</p>


## 🔄 APPLICATION WORKFLOW (USER FLOW)

### ⭐ 1. User Creates an Account (Sign Up Flow)

<img width="1000" height="500" alt="image" src="https://github.com/user-attachments/assets/4cfa2963-48d9-4b74-a336-9ebf4322746e" />

The workflow begins when a new user opens PrepWise and creates an account by entering:

* Name
* Email
* Password

✔ Firebase Authentication securely registers the user

✔ On successful signup, the app shows a success toast

✔ The user is immediately redirected to the Home Dashboard

### ⭐ 2. User Lands on the Home Page

📷 *Insert Home Page Screenshot Here*

Once authenticated, the user sees the Home Page, which shows:

* A welcome header
* “Start an Interview” button
* Sections for **Your Interviews** and **Take Interviews**
* Clean UI with available interview categories (Full Stack, Frontend, Mobile, etc.)

From here, the user can choose to:

* Generate a new interview
* Start an existing interview
* View older results

### ⭐ 3. User Starts Interview Generation (Call 1)

📷 *Insert Interview Generation Call Screenshot Here*

When the user clicks **Start an Interview**, PrepWise triggers **Call 1**, whose purpose is only to *generate interview questions*.

During this call, the AI interviewer asks:

* Role (e.g., Full Stack Developer)
* Interview Type (Technical, Behavioral, Mixed)
* Difficulty Level
* Tech Stack
* Number of Questions

✔ Vapi extracts these values

✔ Sends them to backend

✔ Backend generates a structured list of interview questions using **Google Gemini**

The call ends by saying:
**“Your interview has been generated. You can now take the interview from your dashboard.”**

### ⭐ 4. Dashboard Shows the Generated Interview Cards

📷 *Insert Interview Cards Screenshot Here*

After Call 1 completes, the user is redirected to the dashboard where newly created interviews appear under:

* **Take Interviews** section

Each interview card displays:

* Interview title (e.g., *Full Stack Interview*)
* Date of generation
* Difficulty
* Score (after completion)
* **View Interview** button

The user can now select an interview to begin.

### ⭐ 5. User Takes the Real Interview (Call 2)

📷 *Insert Real Interview Call Screenshot Here*

When the user clicks **View Interview → Start Interview**, PrepWise begins **Call 2**, which is the *actual technical interview*.

In this phase:

* AI interviewer asks the generated technical questions
* User answers via real-time voice conversation
* Vapi transcribes user responses
* Gemini analyzes the answers

The system evaluates:

* Communication
* Technical Strength
* Problem-Solving
* Clarity
* Cultural Fit

The interview continues until all questions are completed.
Finally, the AI says:
**“Thank you for the interview. Your feedback will be generated shortly.”**

### ⭐ 6. User Receives Detailed AI Feedback (Persona-Aware Feedback)

📷 *Insert Feedback Page Screenshot Here*


