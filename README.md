# 🦷 Dental Biometric System  
*A deep-learning based identification system for forensic and administrative dental applications*

---

## 📘 Abstract
The **Dental Biometric System (DBS)** is a user-friendly identification and authentication solution for forensic officers and administrators.  
It automates human identification by analysing **dental radiographs** using deep learning.  
The system applies **VGG16** for feature extraction and **cosine similarity** for feature matching, enabling accurate recognition even when other biometric modalities are unavailable.  
It provides secure data management, efficient record retrieval, and an intuitive desktop interface for daily use within forensic and dental departments.

---

## 🏗️ System Architecture
The project follows a modular architecture:

| Module | Description |
|---------|--------------|
| **User Interface (UI)** | Built with **Kivy**, provides login, data entry, search, update, and identification screens for Admins and Forensic Officers. |
| **Database Layer** | **MySQL** stores dental records, user credentials, and extracted features. |
| **Feature Extraction Module** | Uses **VGG16 CNN** to extract discriminative features from dental radiographs. |
| **Matching Module** | Computes **cosine similarity** between stored and query features for identification. |
| **Controller (main.py)** | Launches and coordinates all modules. |

---

## 🧩 Features
### 👨‍💼 Administrator
- Add, update, or delete individual records and radiographs  
- Register new forensic officers  
- Manage and back-up the database  

### 🕵️‍♂️ Forensic Officer
- Upload radiographs to identify individuals  
- Retrieve age, gender, and ethnicity predictions  
- Search records by date of birth or image  

---

## 🧰 Technology Stack
| Category | Tools / Libraries |
|-----------|------------------|
| Language | **Python 3.11** |
| Deep Learning | **TensorFlow**, **Keras** (VGG16) |
| UI Framework | **Kivy** |
| Database | **MySQL Server** |
| OS Environment | **Linux (Kali)** |
| IDE / Tools | Google Colab (for prototyping), VS Code |

---

## 🧬 Dataset and Model
- **Dataset:** Panoramic dental radiographs (publicly available on Kaggle).  
- **Pre-processing:** Resizing to 224×224 pixels and normalization.  
- **Model:** Pre-trained VGG16 weights used for feature extraction.  
- **Similarity Metric:** Cosine similarity to match ante-mortem and post-mortem records.  
- **Accuracy:** High identification accuracy with average processing time < 3 seconds per image.

---

## ⚙️ Implementation Details
```
Dental-Biometric-System/
├── Dental_Biometric_System/
│ ├── main.py
│ ├── database/
│ ├── feature_extraction/
│ ├── uix/
│ └── Carousel_images/
├── docs/
│ └── Dental_Biometric_System_SRS.pdf
├── requirements.txt
└── README.md
```

---

## 🧪 Testing & Performance Summary
- **Functional Testing:** 7 test cases covering login, CRUD operations, registration, and identification – all passed.  
- **Performance:**  
  - Record retrieval < 2 s  
  - Identification < 3 s per image  
  - 99.5 % uptime target, 99.9 % availability  
- **Security:** User authentication, encrypted data transfer, role-based access control.  

---

## 💻 Installation & Usage
1. **Clone the repository**
   ```bash
   git clone https://github.com/HammadLatif-codes/Dental-Biometric-System.git
   cd Dental-Biometric-System/Dental_Biometric_System

2. **Install dependencies**
   pip install -r requirements.txt

3. **Configure database**
     Create a MySQL database named dental_biometric_system
     Update database/db.py with your DB credentials
   
5. **Run the applicationy**
     python main.py


## 🚀 Future Work
    Integrate direct teeth-scanning hardware for real-time data acquisition.
    Expand dataset to improve accuracy and generalization.
    Add multi-modal biometrics (face + teeth fusion).
    Implement age prediction models from radiographs.
    Develop a web-based interface for remote use.


## 👤 Author

    Hammad Latif
    BS Computer Science — Quaid-i-Azam University, Islamabad
    📧 hammadlatif408@gmail.com
    🔗 GitHub: HammadLatif-codes
