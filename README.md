# Insurance Premium Prediction API

A Machine Learning-powered REST API built with **FastAPI** that predicts insurance premiums based on user-provided information such as age, income, city tier, lifestyle habits, and other risk factors.

## 🚀 Features

* Predict insurance premium using a trained ML model
* Fast and lightweight REST API
* Input validation using Pydantic schemas
* Structured JSON responses
* Error handling and validation
* Docker support for containerized deployment

---

## 📂 Project Structure

```text
insurance_premium_check/
│
├── app.py                 # FastAPI application
├── requirements.txt       # Project dependencies
├── Dockerfile             # Docker configuration
│
├── config/
│   └── city_tier.py       # City tier mapping logic
│
├── model/
│   ├── predict.py         # Prediction logic
│   └── model.pkl          # Trained ML model
│
├── schema/
│   ├── request.py         # Request schema
│   └── response.py        # Response schema
│
└── README.md
```

---

## ⚙️ Installation

### 1. Clone Repository

```bash
git clone https://github.com/v9coder/FastAPI-Tutorial---insurance_premium_api.git
cd FastAPI-Tutorial---insurance_premium_api
```

### 2. Create Virtual Environment

```bash
python -m venv newenv
```

### 3. Activate Virtual Environment

#### Windows

```bash
newenv\Scripts\activate
```

#### Linux / Mac

```bash
source newenv/bin/activate
```

### 4. Install Dependencies

```bash
pip install -r requirements.txt
```

---

## ▶️ Running the API

Start the FastAPI server:

```bash
uvicorn app:app --reload
```

Server will start at:

```text
http://127.0.0.1:8000
```

---

## 📖 API Documentation

FastAPI automatically generates API documentation.

### Swagger UI

```text
http://127.0.0.1:8000/docs
```

### ReDoc

```text
http://127.0.0.1:8000/redoc
```

---

## 🔍 Prediction Endpoint

### POST /predict

Predicts insurance premium based on customer details.

### Sample Request

```json
{
  "age": 21,
  "weight": 72,
  "height": 1.78,
  "income_lpa": 60,
  "smoker": false,
  "city": "Pune",
  "occupation": "private_job"
}
```

### Sample Response

```json
{
  "response": {
    "predicted_category": "Low",
    "confidence": 0.71,
    "class_probabilities": {
      "High": 0.01,
      "Low": 0.71,
      "Medium": 0.28
    }
  }
}
```

---

## 🐳 Docker Support

### Build Docker Image

```bash
docker build -t insurance-premium-api .
```

### Run Container

```bash
docker run -p 8000:8000 insurance-premium-api
```

---

## 🛠 Tech Stack

* Python 3.x
* FastAPI
* Pydantic
* Scikit-Learn
* Pandas
* NumPy
* Uvicorn
* Docker

---

## 📈 Machine Learning Workflow

1. Collect and preprocess insurance data
2. Perform feature engineering
3. Train machine learning model
4. Save trained model using Pickle
5. Load model in FastAPI application
6. Generate premium predictions through API requests

---

## 📌 Future Enhancements

* Authentication and Authorization
* Model Monitoring
* Logging and Analytics
* CI/CD Pipeline
* Cloud Deployment (AWS/Azure/GCP)
* API Rate Limiting

---

## 🙏 Acknowledgements

Special thanks to **CampusX** for their excellent FastAPI tutorial series, which served as a valuable learning resource during the development of this project.

Playlist:
https://www.youtube.com/playlist?list=PLKnIA16_RmvZ41tjbKB2ZnwchfniNsMuQ

This project builds upon the concepts taught in the playlist and includes additional customizations and implementations for insurance premium prediction.

## 👨‍💻 Author

Vinay Pawar

Built as part of a Machine Learning and FastAPI learning project.
