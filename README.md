# CARDIO_VASCULAR-DISEASE-DIAGNOSIS-SYSTEM

🫀 Cardiovascular Disease Expert System
AI Project – Backward & Forward Chaining (C++)

This project implements an Expert System for diagnosing Cardiovascular (Heart) Diseases using Backward Chaining for diagnosis and Forward Chaining for treatment suggestions. It simulates a rule-based inference engine similar to classical AI systems.


📌 Features
✔ Backward Chaining (Diagnosis)
     Asks users questions based on symptoms
     Traverses rules backward from the goal (DISEASE)
     Determines the exact heart-related condition
     Supports multiple diagnostic tests:
     Echo Cardiogram
     Cardiac MRI
     X-Ray
     Blood Test
     ECG
     Stress Test
     CT Scan
     Treadmill Test

✔ Forward Chaining (Treatment)
     Given an identified disease, the system:
     Searches for matching treatment rules
     Produces the correct medical intervention/therapy

📁 Project Structure

├── main.cpp
├── Project1-AI-BackwardChaining.h
├── Project1-AI-BackwardChaining.cpp
├── Project1-AI-ForwardChaining.h
├── Project1-AI-ForwardChaining.cpp
├── Rule_Files/
│   ├── Project1-AI-BWC_Varlist.txt
│   ├── Project1-AI-BWC_Conclist.txt
│   ├── Project1-AI-BWC_Clausevarlist.txt
│   ├── Project1-AI-BWC_ClausevarlistConditions.txt
│   └── Project1-AI-FWC_Clausevarlist.txt
└── README.md

⚙️ How It Works
🧠 Backward Chaining Flow
  Goal starts at: DISEASE
  Engine searches rules where the conclusion is “DISEASE”
  
  For each rule:
    Symptom/variable values are asked from the user
    If a condition requires another derived variable (e.g., ABTEST), that becomes a new sub-goal
  
  Continues until:
    A disease is confirmed
    Or no rules match

⚕️ Forward Chaining Flow (Treatment)
       User provides a disease name
       System scans rules from DISEASE → TREATMENT
       Displays appropriate medical procedures/medications

🚀 Running the Program
1. Compile

Use g++:

g++ main.cpp Project1-AI-BackwardChaining.cpp Project1-AI-ForwardChaining.cpp -o ExpertSystem

2. Run
   ./ExpertSystem


🖥️ User Menu
When the program starts, you will see:

1. Identification of a Cardiovascular(Heart) Disease
2. Treatment for a specific Cardiovascular(Heart) Disease
3. Exit


📌 Supported Diseases

  Angina
  Arrhythmias
  Congenital Heart Disease
  Coronary Heart Disease
  Deep Vein Thrombosis
  Dilated Cardiomyopathy
  Heart Attack
  Heart Failure
  Heart Valve Disease
  Hypertrophic Cardiomyopathy
  Peripheral Arterial Disease
  Stroke


📝 Rule Base Format
Example (Backward Chaining):

  IF SYMPTOM=YES && BREATHLESSNESS=NO && FOOTSORE=YES THEN ABTEST=YES


Example (Forward Chaining):

IF DISEASE=Angina THEN TREATMENT=Angioplastry and Stent treatment...


🔧 Dependencies

  ✔ Standard C++17
  ✔ iostream, fstream, string, map, stack, queue
  ✔ All rule files must be in the project directory


🧪 Example Interaction

  Are you experiencing any symptoms? YES
  Are you experiencing any chest pain? NO
  Are you experiencing cyanosis? YES
  What's the result of Echo cardiogram? ABNORMAL

  You have been diagnosed with CONGENITAL_HEART_DISEASE


📜 License
    This project is free to use for academic and learning purposes.
