Macs-FleetCare 2.0: AI-Driven Predictive Maintenance


![Macs-FleetCare Dashboard](./Macs-FleetCare%202.0%20Homepage/Macs-FleetCare%20Homepage.png)

Macs-FleetCare 2.0 is a full-stack predictive maintenance platform designed to transition from a "proof-of-concept" to a production-ready fleet management solution. This version is engineered for real-world reliability, focusing on early failure detection in passenger vehicle engines (Toyota, Honda, Lexus, etc.).

🔗 Live Project Links
Live Dashboard (Vercel): macs-fleet-care-frontend.vercel.app

API Backend (Render): https://macs-fleetcare-2-0-2.onrender.com

Key Enhancements in 2.0
Authentic Data Foundations: Replaced synthetic data with a real-world automotive dataset (19,000+ records) mirroring genuine sensor profiles.

Safety-First Optimization: Implemented a Risk-Averse Thresholding strategy. By shifting the diagnostic threshold to 30%, the model’s recall for critical failures was boosted from 13% to 56%.

Universal Diagnostic Interface: A vehicle-agnostic UI that allows fleet managers to input raw sensor data (RPM, Oil Pressure, Temperature) for any brand.

Technical Architecture
The project utilizes a decoupled "Two-Repo" architecture for professional scalability:

1. The Brain (Backend)
Framework: FastAPI.

ML Model: XGBoost Classifier optimized with scale_pos_weight and custom probability thresholds.

Deployment: Render.

2. The Face (Frontend)
Framework: React / Vite (via Lovable).

Styling: Modern Dark-Mode SaaS aesthetic with real-time gauges.

Deployment: Vercel.

Model Performance Highlights
Based on our professional evaluation, the 2.0 model prioritizes catching failures (Recall) over raw accuracy, identifying 816 correct failures that would have otherwise gone unnoticed.

Metric,Score
Failure Recall (Class 0),56%
Operational Precision (Class 1),73%
Alert Threshold,30.0%



Project Structure
Macs-FleetCare/
├── main.py               # FastAPI Prediction Logic
├── fleetcare_model.joblib # Trained XGBoost Artifact
├── scaler.joblib          # Feature Normalization Artifact
└── Homepage/             # High-fidelity project assets & UI screenshots


