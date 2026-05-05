HR Wellbeing System
A generative AI application designed to detect burnout risk and support employee wellbeing in organisations.
Author: Khanyisile Planga Course: Generative AI Demo: [https://5006afb1-c8b7-4279-977c-5f54caae7262-00-6lwygc64j25a.janeway.replit.dev/
](https://insidious-deadly-divisor--khanyicollabs.replit.app)
What it does
This system takes anonymised workforce data and uses Google Gemini to analyse burnout risk signals across both quantitative metrics and qualitative survey responses. It produces role-specific outputs for four distinct users, each with different levels of data access enforced at the application level.
•	People Partner sees a full workforce risk report with individual assessments and explanations
•	Team Lead sees an aggregated team dashboard with no individual employee data
•	Employee sees a personal wellbeing summary written in plain, supportive language
•	Compliance Officer sees system-level audit outputs and risk distribution data

Tech stack
•	Python core language
•	Google Gemini 2.5 Flash via the google-genai API for burnout risk analysis and report generation
•	Pandas for data ingestion and processing
•	Streamlit for the user interface
•	Google Colab for development and pipeline testing
•	Replit for deployment

Files
File	Description
app.py	Main Streamlit application
hr_test_3employees.csv	Three employee test datasets used for the prototype demo
	
requirements.txt	Python dependencies

Data
This prototype uses entirely synthetic data generated to reflect realistic HR patterns. No real employee data was used at any stage of development. The synthetic dataset contains 50 rows distributed across three risk categories, high, medium, and low, each with numerical workforce metrics and a free text survey response.

Known limitations
•	The free tier Gemini API has rate limits that require spacing between calls during batch processing
•	The system uses a general-purpose LLM not specifically trained on HR data or validated against clinical burnout frameworks like the Maslach Burnout Inventory
•	LLMs carry a hallucination risk. Human review of all outputs before organisational action is taken is a design requirement
•	The prototype uses synthetic data. A production deployment would require a bias audit before use with real employee data
•	Anonymisation in this prototype uses pseudonymisation. Full anonymisation and a data processing agreement would be required for GDPR compliance in production

Ethical principles
This system was designed around four core principles. Explainability: Every output includes a plain language explanation of the signals that drove it. Privacy: Individual employee data is never visible to managers. Consent, employees have full visibility into what data is collected about them and can flag inaccurate outputs. Accountability: Every system action is logged for audit purposes in line with EU AI Act requirements for high-risk AI systems.





