
# 🏠 RentLense AI

### An Intelligent System for Finding the Right Rental Property

RentLense is an AI-powered rental property search assistant that helps users find suitable rental properties based on their natural-language requirements.

Instead of manually searching through numerous property listings, users can describe what they are looking for in ordinary language. RentLense extracts the important requirements and uses the RentCast API to retrieve relevant rental listings.

## 🚀 Live Application

The RentLense application is deployed using Streamlit Community Cloud.

**Live App:**
[Add your Streamlit application URL here]

---

## 📌 Problem Statement

Finding a suitable rental property can be time-consuming and difficult because rental information is often fragmented across different sources.

Users may need to consider several requirements simultaneously, including:

* Location
* Budget
* Number of bedrooms
* Number of bathrooms
* Property type
* Other preferences

Traditional property searches often require users to repeatedly modify filters and manually compare listings.

RentLense addresses this problem by allowing users to describe their requirements naturally.

---

## 💡 Proposed Solution

RentLense provides an intelligent search interface where users can enter requests such as:

> "I need a 2 bedroom apartment in Austin, Texas under $2,500 per month."

The system processes the request, extracts the relevant requirements, queries the rental property API, and displays available property listings.

---

## 🏗️ System Architecture

```text
User
  │
  ▼
RentLense Streamlit Interface
  │
  ▼
Natural Language Parser
  │
  ▼
Structured Search Requirements
  │
  ▼
RentCast API
  │
  ▼
Rental Property Listings
  │
  ▼
Results Display
```

---

## 🔧 Technologies Used

* **Python** — Core programming language
* **Streamlit** — Web application interface
* **Pandas** — Data processing
* **Requests** — API requests
* **python-dotenv** — Local environment variable management
* **RentCast API** — Rental property data source
* **GitHub** — Source code management
* **Streamlit Community Cloud** — Application deployment

---

## 📂 Project Structure

```text
RentLense_Capstone/
│
├── app.py
├── requirements.txt
├── README.md
├── .gitignore
│
├── services/
│   ├── parser.py
│   ├── rentcast.py
│   └── __init__.py
│
└── tests/
    └── ...
```

---

## 🔄 How RentLense Works

### 1. User Input

The user enters a natural-language rental request.

Example:

```text
I need a 2 bedroom apartment in Austin, Texas under $2,500 per month.
```

### 2. Requirement Extraction

The parser identifies relevant requirements such as:

```text
City: Austin
State: Texas
Bedrooms: 2
Maximum Price: $2,500
```

### 3. API Search

The structured requirements are sent to the RentCast API.

### 4. Property Retrieval

RentCast returns available rental property listings matching the search criteria.

### 5. Results

RentLense displays the retrieved properties to the user.

---

## 🔐 Security

The RentCast API key is not stored directly in the source code.

For local development, environment variables are used.

For deployment, the API key is stored using Streamlit Secrets.

The `.env` file is excluded from Git using `.gitignore`.

---

## ▶️ Running the Project Locally

### Clone the repository

```bash
git clone YOUR_GITHUB_REPOSITORY_URL
```

### Navigate into the project

```bash
cd RentLense_Capstone
```

### Create a virtual environment

```bash
python -m venv .venv
```

### Activate the environment on Windows

```powershell
.venv\Scripts\activate
```

### Install dependencies

```bash
pip install -r requirements.txt
```

### Configure the API key

Create a `.env` file:

```text
RENTCAST_API_KEY=your_rentcast_api_key
```

### Run the application

```bash
streamlit run app.py
```

---

## 🧪 Testing

The application was tested locally and after deployment.

Testing confirmed that:

* The Streamlit application loads successfully.
* Natural-language rental requirements can be entered.
* Requirements are processed by the parser.
* RentCast API requests are successfully completed.
* Rental property results are returned.
* The deployed application successfully performs live searches.

---

## 🌐 Deployment

RentLense is deployed using Streamlit Community Cloud.

The application uses Streamlit Secrets to securely provide the RentCast API key during deployment.

---

## 🎯 Future Improvements

Future versions of RentLense could include:

* Personalized property ranking
* Property recommendation scores
* Saved searches
* User accounts
* Property comparison
* Map-based property visualization
* Commute-time analysis
* More advanced natural-language understanding
* Additional rental data sources
* User feedback for improving recommendations

---

## 👨‍💻 Project

**Project:** RentLense AI
**Purpose:** Intelligent rental property search
**Deployment:** Streamlit Community Cloud

