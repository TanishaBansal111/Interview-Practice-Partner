
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

<p align="center" style="margin: 30px 0;"><img width="800" height="450" alt="image" src="https://github.com/user-attachments/assets/4cfa2963-48d9-4b74-a336-9ebf4322746e" /></p>


The workflow begins when a new user opens PrepWise and creates an account by entering:

* Name
* Email
* Password

✔ Firebase Authentication securely registers the user

✔ On successful signup, the app shows a success toast

✔ The user is immediately redirected to the Home Dashboard

### ⭐ 2. User Lands on the Home Page

<p align="center" style="margin: 30px 0;"><img width="800" height="450" alt="image" src="https://github.com/user-attachments/assets/15abee28-6fd7-47b1-8f30-8d4adece3df7" />
</p>


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

<p align="center" style="margin: 30px 0;"><img width="800" height="450" alt="image" src="https://github.com/user-attachments/assets/84b0a45e-52ec-4cb4-bd61-d3bd9f0b709c" /></p>


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

<p align="center" style="margin: 30px 0;"><img width="800" height="450" alt="image" src="https://github.com/user-attachments/assets/75ba6502-7145-40c5-9bac-4530988689ab" /></p>


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

<p align="center" style="margin: 30px 0;"><img width="800" height="450" alt="image" src="https://github.com/user-attachments/assets/12581f45-d2b2-4ad0-9b5f-6376eda2455e" /></p>


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

Once the interview ends, PrepWise generates a personalized AI-driven feedback report using Google Gemini.
The feedback dynamically adapts based on how the user behaved during the interview.

PrepWise supports four user personas, each producing unique feedback styles.

🟣 Persona 1 — Efficient User

📌 This persona gives quick and structured answers.

<p align="center" style="margin: 30px 0;"> <img width="800" height="450" alt="image" src="https://github.com/user-attachments/assets/1cf43f01-b9d6-4407-a2bd-50472240cdb3" />
  <img width="800" height="450" alt="image" src="https://github.com/user-attachments/assets/ac93d6a4-e425-488d-87f3-dc38fc129df3" />

</p>

🔍 Behaviour

* Gives short, crisp, highly relevant answers

* Doesn’t waste time; goes directly to the point

* Uses structured explanations

📝 Feedback Highlights

* Strong communication clarity

* Good technical depth

* Good confidence

* Suggested improvement: add more examples or elaboration

🔵 Persona 2 — Confused User

📌 This persona is unsure and asks clarifying questions repeatedly.

<p align="center" style="margin: 30px 0;"><img width="800" height="450" alt="image" src="https://github.com/user-attachments/assets/d9079000-1d2e-44ab-8f79-98eb6b07690d" />
<img width="800" height="450" alt="image" src="https://github.com/user-attachments/assets/607e05ec-8991-4b7e-afa3-49a0874fb4b6" />
</p>


🔍 Behaviour

* Frequently asks “Sorry, what does that mean?”

* Repeats the question instead of answering

* Low clarity, uncertain tone

📝 Feedback Highlights

* Lower communication & clarity score

* Encouragement to organize thoughts

* Suggestion to use the STAR method

* Recommended to strengthen core basics

🟡 Persona 3 — Chatty User

📌 This persona talks too much and often goes off-topic .

👉 Insert Chatty User screenshot here:

🔍 Behaviour

* Gives very long answers

* Goes off-topic frequently

* Adds unnecessary stories

📝 Feedback Highlights

* Needs more concise responses

* Should focus on structured answers

* Encouraged to reduce irrelevant details

* Shows enthusiasm but lacks precision

🔴 Persona 4 — Edge-Case User
(Nonsense Inputs, Invalid Answers)

📌 This persona gives irrelevant, contradictory, or nonsensical answers that push the AI outside normal conversation boundaries.

👉 Insert Edge-Case User screenshot here:

🔍 Behaviour

* Gives unrelated / incomplete responses

* Sometimes intentionally gives wrong patterns

* Tests system limits

📝 Feedback Highlights

* Feedback focuses on correctness

* Suggests answering with real examples

* Encourages sticking to question context



