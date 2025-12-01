# Aidentis AI Dental Diagnostics Platform

Aidentis is an AI-powered dental diagnostics platform designed to enhance clinical precision, streamline orthodontic workflows, and improve patient communication. The system provides instant lateral cephalogram analysis, automated CBCT interpretation, and accurate 3D model generation to support modern orthodontic and diagnostic practices.

Website: https://aidentis.cc/  
Contact: assylzat@aidentis.cc

---

## 🚀 Key Features

- **Instant Cephalometric Analysis**  
  Automated landmark detection and measurement extraction for orthodontic assessments.

- **CBCT Scan Interpretation**  
  AI-driven volumetric analysis, anatomical structure detection, and diagnostic insights.

- **3D Model Reconstruction**  
  Converts 2D and 3D imaging data into interactive models for treatment planning.

- **Patient Communication Tools**  
  Visual treatment simulations to help explain orthodontic conditions and options.

- **Workflow Automation**  
  Reduces manual tasks, shortens diagnostic time, and standardizes evaluation across clinics.

---

## 🧠 AI & ML Capabilities

- Deep learning models for medical image segmentation and landmark detection  
- 3D CNNs for volumetric CBCT interpretation  
- Generative models for reconstruction and visualization  
- Continual learning framework for model updates  
- Quality control pipeline to filter poor-quality input images

---

## ☁️ Google Cloud Architecture

Aidentis is built on a secure, scalable cloud-native stack:

- **Vertex AI** → Model training, tuning, and deployment  
- **Cloud Run** → Serverless inference endpoints  
- **Cloud Storage** → Encrypted medical imaging storage  
- **Cloud Functions** → Automated preprocessing and pipeline orchestration  
- **Firestore / Cloud SQL** → Clinic and patient metadata  
- **Cloud IAM** → Role-based access control  
- **Cloud Logging & Monitoring** → Full observability  

All components comply with healthcare-grade data protection requirements and regional regulations.

---

## 🏗️ Platform Architecture Overview

Dentist Uploads Scan → Preprocessing → AI Inference (GCP) → 2D/3D Output
↓ ↓
Ceph Points CBCT Interpretation
↓ ↓
Diagnostic Report ← Visualization Engine ← 3D Reconstruction

---

## 🛠️ Installation & Setup (Local / Developer Mode)

### 1. Clone Repository
```bash
git clone https://github.com/yourusername/Aidentis-AI-Dental-Diagnostics-Platform.git
cd Aidentis-AI-Dental-Diagnostics-Platform
pip install -r requirements.txt
GCP_PROJECT_ID=your_project_id
GCP_BUCKET_NAME=your_bucket
MODEL_ENDPOINT=your_vertex_ai_endpoint
uvicorn app.main:app --reload
POST /api/upload
Content-Type: multipart/form-data
POST /api/ceph/analyze
POST /api/cbct/analyze
POST /api/3d/reconstruct
