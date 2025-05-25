# Coding Week 2025 – Machine Learning Challenge 

Welcome to the official repository for **Coding Week 2025 – ML Challenge** organized by the Coding Club, IIT Guwahati. This repo showcases two key tasks:

1. **CampusPulse** – Predicting student relationships using anonymized behavioral data.
2. **WeatherMind** – Building an agentic AI assistant with reasoning, perception, and tool integration.

---

##  Task 1: CampusPulse

###  Objective
Predict if a student is in a romantic relationship based on behavioral and academic data.

###  Workflow

#### 🔹 Level 1: Variable Identification
- Interpreted anonymized features (`Feature_1`, `Feature_2`, `Feature_3`) using statistical and visual patterns.
- Example mappings:
  - `Feature_1` → Social media usage
  - `Feature_2` → Study hours
  - `Feature_3` → Sleep quality

#### 🔹 Level 2: Data Integrity Audit
- Detected missing values using `missingno` plots.
- Imputed missing data using strategies like:
  - KMeans clustering for `Feature_1`
  - Median for `Screen Time`
  - KNN imputation for `GPA`

#### 🔹 Level 3: Exploratory Insights
- Answered questions like:
  - Does GPA correlate with screen time?
  - How does stress relate to sleep?
  - Does gender affect screen time?
- Visuals: Heatmaps, bar charts, violin plots, and line graphs.

#### 🔹 Level 4: Relationship Prediction
- Trained:
  - Logistic Regression (Accuracy: ~63.8%)
  - Random Forest (Accuracy: ~71%)
- Used `GridSearchCV` for tuning hyperparameters.

#### 🔹 Level 5: Interpretability with SHAP
- Top features: Emotional health, GPA, Sleep, Screen time.
- Visualized local & global SHAP explanations.
- Compared decision boundaries across models.

---

##  Task 2: WeatherMind 🌦️

###  Objective
Build an **agentic AI assistant** using **LangGraph** that can:
- Reason through tools
- Perceive external context
- Hold memory across interactions

###  Architecture

####  Level 1: Core LLM + Calculator Tool
- Integrated an LLM node with a custom calculator for BODMAS-based queries.

####  Level 2: Perception Tools
- **Fashion Recommender** (mocked by city): e.g., Tokyo → oversized blazers.
- **Weather Extractor** using OpenWeatherMap API.

####  Level 3: Judgement + Memory
- Implemented tool routing logic for math, fashion, and weather queries.
- Added memory with `ConversationBufferMemory` to retain context.

####  Level 4: Multi-Agent System
- Created 3 LangGraph agents:
  - Query Classifier
  - Data Fetcher
  - Response Synthesizer
- Added an **Event Planner Tool** (mock) to combine tools smartly.
- Visualized LangGraph with `draw_graph()`.

---

## 🛠️ Tech Stack

- Python
- Pandas, NumPy, Scikit-learn
- Matplotlib, Seaborn
- SHAP, NetworkX
- LangGraph (LLM + tool orchestration)
- OpenWeatherMap API
- Jupyter Notebook

---




