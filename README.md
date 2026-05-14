# assignment-1-AI
Assignment 1: AI System Specification
Course: Introduction to Artificial Intelligence
Topic: PEAS Framework and Task Environment Analysis
Objectives
The goal of this assignment is to apply the formal frameworks from Russell & Norvig (Chapter 2)
to a real-world problem. You will demonstrate your ability to specify success metrics, classify the
complexity of an AI’s operational environment, and represent AI system information in a structured
data format.
Task Description
Select one of the following modern AI applications:
• A: An Automated Warehouse Sorting Robot (e.g., Amazon Robotics).
• B: A Personalized News Feed Recommender (e.g., Twitter/X or TikTok algorithm).
• C: An Agricultural Monitoring Drone for crop disease detection.
• D: A Medical Imaging Assistant for early disease detection (e.g., X-ray triage).
• E: A Smart Traffic Signal Controller for reducing congestion in cities.
• F: A Voice-Based Virtual Assistant for multilingual customer support.
• G: A Fraud Detection System for digital payments and banking transactions.
• H: An AI Tutor for personalized student learning recommendations.
• I: A Predictive Maintenance System for factory machines and equipment.
• J: A Disaster Response Drone for search, mapping, and emergency support.
For your chosen system, complete the following four tasks:
Task 1: PEAS Specification
Define the PEAS framework for your agent. Ensure your descriptions are specific (e.g., do not just
say ”Cameras,” specify ”High-resolution RGB and Infrared sensors”).
Performance Measure: How exactly is success measured? List at least four metrics.
Environment: Where does the agent act? What are the key external factors?
Actuators: What physical or digital tools does the agent use to change its world?
Sensors: What are the inputs the agent uses to perceive its state?
Task 2: Environment Classification
Classify the task environment according to the following dimensions. For each, provide a onesentence justification explaining your choice.
• Fully Observable vs. Partially Observable
1
• Single-agent vs. Multi-agent
• Deterministic vs. Stochastic
• Episodic vs. Sequential
• Static vs. Dynamic
• Discrete vs. Continuous
Task 3: Critical Analysis
Answer the following questions in short-paragraph format:
1. Which of the six dimensions mentioned in Task 2 poses the greatest technical challenge
for an AI engineer building this system? Why?
2. Propose one Utility Function that would help the agent handle a trade-off (e.g., Speed vs.
Safety). How would the agent’s behavior change if the weight of this utility was doubled?
Task 4: Structured Data Design (JSON Practice)
Represent your Task 1 and Task 2 outputs in a single valid JSON object. This task is for practicing
structured data storage and machine-readable AI specifications.
Requirements:
• Include top-level keys: system_name, peas, environment_classification, utility_function.
• Under peas, include: performance_measures, environment, actuators, sensors.
• Store performance_measures as an array with at least 4 items.
• Store each environment dimension as a nested object with fields choice and justification.
• Ensure your JSON is syntactically valid (proper quotes, commas, and brackets).
Suggested JSON template (adapt with your own content):
{
"system_name": "Agricultural Monitoring Drone",
"peas": {
"performance_measures": [
"disease_detection_accuracy",
"false_alarm_rate",
"coverage_per_hour",
"battery_efficiency"
],
"environment": "Large open farmland with variable weather",
"actuators": ["flight_controller", "sprayer"],
"sensors": ["RGB_camera", "infrared_camera", "GPS"]
},
"environment_classification": {
2
"observability": {
"choice": "Partially Observable",
"justification": "Occlusion and weather hide some crop regions"
},
"agents": {
"choice": "Single-agent",
"justification": "Only one primary decision-making drone"
}
},
"utility_function": "U = 0.6*accuracy - 0.4*energy_cost"
}
Submission Guidelines
• Submit your response as a single PDF file via email.
• Include your JSON output in a separate section titled Structured Representation.
• Format: 12pt font, maximum 3 pages.
• Academic Integrity: All justifications must be your own. Use of AI for formatting is allowed,
but the design logic must be original.
3
