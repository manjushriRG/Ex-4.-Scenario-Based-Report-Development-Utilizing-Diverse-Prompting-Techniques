
# Ex-4: Scenario-Based Report Development Utilizing Diverse Prompting Techniques

## Aim

The aim of this experiment is to design, test, and analyze an **AI-powered virtual health assistant** capable of supporting patients in healthcare contexts. The assistant should efficiently handle health-related FAQs, set up medication reminders, and provide basic lifestyle guidance while ensuring accuracy, empathy, and safety. This experiment evaluates different prompting strategies to identify the **most effective technique** for real-world healthcare chatbot deployment.

---

## Introduction

Healthcare systems today face increasing pressure due to rising patient numbers, shortage of medical staff, and demand for **24/7 medical guidance**. AI-driven virtual assistants provide a scalable solution by offering:

* Instant responses to **common medical questions**.
* Reminders for **medications, appointments, and follow-ups**.
* Personalized health and lifestyle suggestions.
* Reduction of **doctor-patient communication burden** for minor or repetitive queries.

However, the **quality of AI responses** depends significantly on the **prompting method** used. A poorly designed prompt may generate unsafe, vague, or impersonal responses, which can **damage patient trust**. On the other hand, carefully crafted prompts allow the assistant to give **accurate, empathetic, and patient-centric replies**.

This study tests **five prompting techniques**—zero-shot, few-shot, role-based, chain-of-thought, and reflective prompting—across two real-world scenarios:

1. **Medication Reminder Setup**
2. **Symptom Inquiry**

Each technique is evaluated on accuracy, relevance, personalization, and patient experience.

---

## Scenario 1: Medication Reminder

**Situation:**
A patient, Meera, is prescribed **Metformin** for diabetes management and wants the assistant to set a daily reminder at **8 AM**.

**Assistant Requirements:**

* Recognize medicine name and dosage timing.
* Confirm correct scheduling.
* Communicate politely and reassuringly.

### Prompting Techniques Applied

* **Zero-Shot:**
  → Gave a vague response: *“I can remind you about medications. Please check your phone alarm.”*
  → Failed to create reminder and lacked personalization.

* **Few-Shot:**
  → With examples of similar queries, it replied: *“Reminder set for Metformin at 8 AM daily.”*
  → Accurate, but sounded robotic.

* **Role-Based:**
  → Assigned role as a **virtual healthcare assistant**:
  *“Hello Meera! I’ve set a reminder for your Metformin at 8 AM every day. Would you like me to also track missed doses?”*
  → Warmer and more patient-friendly.

* **Chain-of-Thought:**
  → Reasoned step-by-step: identified medicine → confirmed time → established repetition → reassured user:
  *“Meera, I’ve scheduled a daily reminder for your Metformin at 8 AM. I’ll notify you every morning and keep track if you miss a dose.”*
  → Provided complete and logical response.

* **Reflective Prompting:**
  → Evaluated first draft and improved empathy:
  *“Your health is important, Meera. I’ve set a daily reminder for Metformin at 8 AM. If you ever miss a dose, I’ll check in and remind you again. Would you like me to send weekly adherence summaries?”*
  → Balanced accuracy, empathy, and proactive care.

**Performance Table – Medication Reminder**

| Technique        | Accuracy | Relevance | Personalization | User Experience |
| ---------------- | -------- | --------- | --------------- | --------------- |
| Zero-Shot        | ★★☆☆☆    | ★★☆☆☆     | ★☆☆☆☆           | ★★☆☆☆           |
| Few-Shot         | ★★★★☆    | ★★★★☆     | ★★★☆☆           | ★★★★☆           |
| Role-Based       | ★★★★☆    | ★★★★☆     | ★★★★☆           | ★★★★☆           |
| Chain-of-Thought | ★★★★★    | ★★★★★     | ★★★★☆           | ★★★★★           |
| Reflective       | ★★★★☆    | ★★★★★     | ★★★★★           | ★★★★★           |

---

## Scenario 2: Symptom Inquiry

**Situation:**
Raj reports: *“I have a headache and a slight fever. Should I be worried?”*

**Assistant Requirements:**

* Show empathy for discomfort.
* Provide **safe and responsible guidance**.
* Suggest when to escalate to a doctor.

### Prompting Techniques Applied

* **Zero-Shot:**
  → Replied: *“Headache and fever are common. Please drink water.”*
  → Too generic and medically unsafe.

* **Few-Shot:**
  → With examples, it improved:
  *“I understand you have headache and fever. Please rest and stay hydrated. Monitor your temperature.”*
  → Helpful but incomplete.

* **Role-Based:**
  → As a nurse assistant:
  *“Raj, I’m sorry you’re not feeling well. A mild fever with headache may be due to flu or cold. Please rest, drink fluids, and monitor your temperature. If it lasts more than 2 days or rises above 101°F, consult a doctor.”*
  → Empathetic and professional.

* **Chain-of-Thought:**
  → Logical reasoning: identify → analyze severity → safe response → escalation:
  *“Since your fever is mild, rest and hydration should help. However, if the fever rises above 101°F, lasts more than 48 hours, or comes with severe symptoms, please seek medical attention immediately.”*
  → Clear and responsible.

* **Reflective Prompting:**
  → Self-corrected to add more care:
  *“Raj, I know this must be uncomfortable. Please rest, drink fluids, and monitor your fever closely. If it persists beyond 2 days or worsens, see a doctor right away. Would you like me to set a reminder to check your symptoms tomorrow?”*
  → Empathy + proactive support.

**Performance Table – Symptom Inquiry**

| Technique        | Accuracy | Relevance | Personalization | User Experience |
| ---------------- | -------- | --------- | --------------- | --------------- |
| Zero-Shot        | ★★☆☆☆    | ★★☆☆☆     | ★☆☆☆☆           | ★☆☆☆☆           |
| Few-Shot         | ★★★☆☆    | ★★★★☆     | ★★★☆☆           | ★★★☆☆           |
| Role-Based       | ★★★★☆    | ★★★★☆     | ★★★★☆           | ★★★★☆           |
| Chain-of-Thought | ★★★★★    | ★★★★★     | ★★★★☆           | ★★★★★           |
| Reflective       | ★★★★☆    | ★★★★★     | ★★★★★           | ★★★★★           |

---

## Comparative Analysis

Across both scenarios:

* **Zero-Shot** → performed poorly with vague or unsafe responses.
* **Few-Shot** → provided structured answers but lacked empathy and depth.
* **Role-Based** → gave the assistant a professional identity, making responses **more empathetic and trustworthy**.
* **Chain-of-Thought** → excelled in logical reasoning and delivering **step-by-step safe recommendations**.
* **Reflective Prompting** → added self-correction, empathy, and personalization, making it ideal for healthcare use.

---

## Results

The assistant was tested with additional queries such as:

* “What should I eat for a low-sugar diet?”
* “Can you remind me of my doctor appointment tomorrow at 4 PM?”
* “I feel tired after exercise—what should I do?”

Findings:

1. **Zero-Shot Prompting**

   * Weak performance, often too general or risky.
   * Unsuitable for healthcare beyond basic FAQs.

2. **Few-Shot Prompting**

   * More accurate with examples, but **still lacked trust-building tone**.

3. **Role-Based Prompting**

   * Created consistency in assistant’s persona (like a nurse/health coach).
   * Increased user trust significantly.

4. **Chain-of-Thought Prompting**

   * Best suited for **diagnostic-like reasoning tasks**.
   * Delivered structured and actionable advice.

5. **Reflective Prompting**

   * Produced **empathetic, polished, and self-corrected responses**.
   * Best for maintaining patient satisfaction and safety.

**Performance Comparison Table**

| Prompting Technique | Accuracy | Relevance | Personalization | User Experience | Overall Effectiveness |
| ------------------- | -------- | --------- | --------------- | --------------- | --------------------- |
| Zero-Shot           | ★★☆☆☆    | ★★☆☆☆     | ★☆☆☆☆           | ★★☆☆☆           | Low                   |
| Few-Shot            | ★★★★☆    | ★★★★☆     | ★★★☆☆           | ★★★★☆           | Medium                |
| Role-Based          | ★★★★☆    | ★★★★☆     | ★★★★☆           | ★★★★☆           | High                  |
| Chain-of-Thought    | ★★★★★    | ★★★★★     | ★★★★☆           | ★★★★★           | Very High             |
| Reflective          | ★★★★☆    | ★★★★★     | ★★★★★           | ★★★★★           | Very High             |

---

## Conclusion

This experiment highlights that **prompting methods strongly influence AI assistant effectiveness in healthcare**.

* **Zero-shot prompting** was inadequate for sensitive scenarios.
* **Few-shot prompting** improved accuracy but remained limited.
* **Role-based prompting** created trust and empathy, essential in healthcare.
* **Chain-of-thought prompting** excelled in **complex reasoning and structured guidance**.
* **Reflective prompting** ensured **accuracy, empathy, and proactive care** by revising and refining its answers.

**Final Inference:**
For healthcare assistants, the **combination of chain-of-thought and reflective prompting** offers the most reliable, empathetic, and patient-centered performance. These techniques ensure safety, accuracy, and positive user experience—critical for healthcare environments.

---

