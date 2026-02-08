# Devina-safety-map
🌸 Devina — A Context-Aware Women’s Safety Companion (Prototype)

Devina is a prototype web application that explores how contextual, real-world signals can be combined to provide an interpretable indication of situational safety for a given location.
The project focuses on system design, transparency, and reliability, rather than prediction accuracy or automation.

🧠 Motivation

Women’s safety is highly contextual and a matter of great concern in the area that I live in and also in many countries across the globe. The same place can feel very different depending on time of day, surrounding activity, access to emergency services, and infrastructure such as lighting or transport.
Most safety-related applications focus on reactive alerts. Deviina was built to explore a proactive, informational approach — helping users reason about their surroundings using clearly explained signals, while avoiding false certainty.

⚙️ How It Works (High Level)

Devina computes a safety score by combining four primary signals:
 Temporal Risk
Time of day is used as a proxy for activity levels and visibility.
 Emergency Proximity
Distance to nearby hospitals and police stations using open map data.
 Activity Density
Presence of shops, restaurants, and public venues as a proxy for human presence.
 Infrastructure Availability
Indicators such as street lighting and access to public transport.
Each signal contributes to a rule-based, weighted scoring system designed for interpretability and clarity.

🧩 System Architecture

 Frontend
 
A simple HTML interface for user interaction and visualization.

 Backend
 
A Flask-based server handling requests, validation, and real-time updates.
 Safety Engine
A separate logic module responsible for:
 External data retrieval
 Distance calculations
 Risk scoring
 Service availability detection
 Communication
 Both REST APIs and real-time updates using WebSockets.
 Data Sources
 OpenStreetMap (via Overpass API) and IP-based geolocation services.

🧠 Design Philosophy

Interpretability over black-box models
    A rule-based approach was chosen instead of machine learning to keep the system explainable and auditable.
Graceful degradation
    If required data sources are unavailable, the system explicitly reports a “service unavailable” state instead of guessing.
Separation of concerns
    The application is structured into distinct layers (UI, backend, safety logic) to support focused learning and maintainability.
Ethical caution
    The system avoids framing results as guarantees and emphasizes context rather than prediction.

🤖 Use of AI Tools

AI-assisted tools were used during development as implementation and iteration aids.

My role focused on:

Defining the problem and constraints
Designing the safety logic and scoring structure
Selecting data sources and validation rules
Evaluating outputs and handling edge cases
Iterating on system behavior and failure handling
This project was also used as a learning exercise to study and understand the concepts introduced during development.

📚 What I Learned

Through this project, I explored and learned:
Web application fundamentals (HTTP, REST APIs, client–server architecture)
Backend development using Python and Flask
Real-time systems using WebSockets
External API integration and defensive programming
Basic geospatial reasoning and distance calculations
Rule-based scoring systems and reliability-focused design
The learning process was problem-driven — concepts were studied as they became necessary to solve specific challenges.

⚠️ Limitations & Ethical Notes

The safety score is indicative, not a guarantee of personal safety.
Data availability varies significantly by region.
The system avoids making inferences when data is insufficient to reduce false confidence.
This project is a prototype and is not intended for real-world deployment without expert review and validation.

🚀 Future Improvements

Localized calibration using regional data
User feedback integration
Improved explainability of individual score components
Offline and low-connectivity support
Stronger privacy and data minimization practices
