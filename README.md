# 🚀 MLOps with MLflow and DagsHub

This project demonstrates an end-to-end **MLOps workflow** using **MLflow** for experiment tracking and **DagsHub** for remote model management, tracking, and collaboration. The pipeline trains a regression model (ElasticNet) on the wine quality dataset and tracks parameters, metrics, and model artifacts using MLflow with remote logging enabled on DagsHub.

---

## 📌 Key Features

- ✅ ML experiment tracking with **MLflow**
- ✅ Remote experiment logging with **DagsHub**
- ✅ Parameter and metric logging
- ✅ Model versioning and comparison
- ✅ Visual insights via MLflow UI and DagsHub Experiments tab

---

## 🔧 Project Structure
├── app.py
├── requirements.txt
├── README.md
├── mlruns/
├── venv/
└── ...

app.py: Main application script.

requirements.txt: Python dependencies.

mlruns/: Directory where MLflow stores experiment logs.

venv/: Virtual environment directory.🧪 MLflow Experiments
We train two ElasticNet models with different hyperparameters (alpha, l1_ratio) and compare their performance.

✅ Experiments on DagsHub
You can compare model runs directly in the DagsHub UI under the Experiments tab.


✅ MLflow UI Dashboard
Run mlflow ui locally or view experiments directly from the DagsHub-hosted MLflow interface.


📈 Metrics Comparison
Run Name	Alpha	L1 Ratio	MAE	R2	RMSE
silent-yak-854	0.3	0.7	0.608	0.149	0.774
gentle-hare-904	0.5	0.5	0.627	0.108	0.793

🛠️ How to Run
Clone the repo:

bash
Copy
Edit
git clone https://github.com/vijayaragavaan2065/MLOPS-with-Mlflow-and-Dagshub.git
cd MLOPS-with-Mlflow-and-Dagshub
Install dependencies:

bash
Copy
Edit
pip install -r requirements.txt
Set MLflow Tracking URI to DagsHub:

Replace the placeholders with your DagsHub credentials.

python
Copy
Edit
mlflow.set_tracking_uri("https://dagshub.com/<your-username>/<your-repo>.mlflow")
mlflow.set_experiment("Default")

mlflow.set_registry_uri("https://dagshub.com/<your-username>/<your-repo>.mlflow")
os.environ['MLFLOW_TRACKING_USERNAME'] = "<your-username>"
os.environ['MLFLOW_TRACKING_PASSWORD'] = "<your-personal-access-token>"
Run the script:

bash
Copy
Edit
python app.py
View results:

Local MLflow UI: http://localhost:5000

DagsHub UI:

![image](https://github.com/user-attachments/assets/2b0afc6e-821f-4760-a2c5-fab08d8c525a)


📂 Sample Output Screenshots

![image](https://github.com/user-attachments/assets/9b9cd84d-5573-47fc-8053-ba85888cc566)
![image](https://github.com/user-attachments/assets/81278cdd-60a2-4499-b700-f2ea37aa36ea)


DagsHub Experiment Comparison

![image](https://github.com/user-attachments/assets/0e2fa559-2957-4e59-9364-b29870b03bb6)
![image](https://github.com/user-attachments/assets/c4e6c819-7ace-44bc-be5c-f7772ad1e9e4)




