# 🔐 Network Security – Intrusion Detection System

A machine learning–based **network intrusion detection system (IDS)** designed to classify and predict malicious activities from network traffic. This project integrates data preprocessing, model training, prediction, and deployment into a single pipeline, with a web interface for real-time detection.

---

## 📌 Features

* **Data ingestion & validation**: Handles raw network data, validates schema, and prepares features.
* **Machine learning models**: Trains and evaluates multiple ML algorithms (Logistic Regression, Random Forest, XGBoost, etc.) with hyperparameter tuning.
* **Prediction pipeline**: Generates predictions for new/unseen network traffic.
* **Database integration**: Uses **MongoDB** for storing datasets and logs.
* **Web app**: Flask-based interface (`app.py`) for uploading data and viewing predictions.
* **Docker support**: Containerized for easy deployment.

---

## 🏗️ Project Structure

```
Network-Security/
│
├── Network_Data/           # Raw dataset files
├── valid_data/             # Cleaned & validated data
├── prediction_output/      # Model prediction results
├── final_model/            # Trained model artifacts
├── data_schema/            # Schema definitions for validation
├── networksecurity/        # Core package (data handling, training, utils)
├── templates/              # HTML templates for Flask web app
│
├── app.py                  # Flask app for web interface
├── main.py                 # Training & pipeline execution
├── push_data.py            # Script to push data to MongoDB
├── test_mongodb.py         # MongoDB connectivity test
├── requirements.txt        # Python dependencies
├── setup.py                # Package setup
├── Dockerfile              # For containerization
└── README.md               # Project documentation
```

---

## ⚙️ Installation & Setup

### 1. Clone the repository

```bash
git clone https://github.com/gator-ryan/Network-Security.git
cd Network-Security
```

### 2. Create and activate virtual environment

```bash
python -m venv venv
source venv/bin/activate   # Linux/Mac
venv\Scripts\activate      # Windows
```

### 3. Install dependencies

```bash
pip install -r requirements.txt
```

### 4. Setup MongoDB

* Ensure you have a **MongoDB instance** running (local or cloud e.g. Atlas).
* Update the MongoDB connection URI in your configuration files.
* Test connection:

```bash
python test_mongodb.py
```

### 5. Run the application

```bash
python app.py
```

Visit: **[http://127.0.0.1:5000/](http://127.0.0.1:5000/)**

---

## 🚀 Docker Deployment

To build and run the Docker container:

```bash
docker build -t network-security .
docker run -p 5000:5000 network-security
```

---

## 📊 Dataset

* The system can be trained on public intrusion detection datasets such as **NSL-KDD**, **CICIDS 2017**, or custom network traffic logs.
* Place datasets in `Network_Data/` and define schema in `data_schema/`.

---

## 🔎 Example Usage

1. Upload a CSV file containing network features via the web interface.
2. The system preprocesses the file, validates schema, and applies the trained ML model.
3. Results (benign/malicious classification) are displayed in the browser and saved to `prediction_output/`.

---

## 🧪 Testing

* Unit and integration tests should be expanded.
* Run basic connectivity tests:

```bash
pytest
```

---

## 📌 Roadmap

* [ ] Add more ML/DL models (CNN, LSTM for sequence data).
* [ ] Improve visualization of predictions and attack statistics.
* [ ] Integrate real-time packet capture.
* [ ] Expand test coverage.
* [ ] Deploy to cloud (AWS/GCP/Azure).

---

## 🤝 Contributing

Contributions are welcome! Please fork this repo and submit a pull request with improvements.

---

## 📜 License

This project is licensed under the **MIT License** – see the [LICENSE](LICENSE) file for details.

---

## 👨‍💻 Author

**Narayan Singh Bhadauriya**
📧 narayansbhadauriya@gmail.com
🔗 https://github.com/gator-ryan/
LinkedIn: www.linkedin.com/in/nsbhadauriya/
