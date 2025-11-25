# 🔬 Melanom AI - Sistem de Detecție a Melanomului folosind Rețele Neuronale

**Disciplina:** Rețele Neuronale  
**Instituție:** POLITEHNICA București – FIIR  
**Student:** Dumitru Claudia Ștefania  
**Data:** Noiembrie 2024  

---

## 📋 Descriere Proiect

Acest proiect implementează un sistem de **inteligență artificială** pentru **detectarea și clasificarea melanomului** din imagini dermatoscopice. Sistemul utilizează tehnici de **Deep Learning** și **rețele neuronale convoluționale (CNN)** pentru a diferenția între leziunile cutanate benigne și maligne.

### Obiective:
- Clasificarea automată a leziunilor cutanate (benign vs. malign)
- Analiza imagistică pentru detectarea precoce a melanomului
- Implementarea unui model CNN eficient și precis

---

## 📁 Structura Proiectului

```
Melanom_AI/
├── README.md                    # Documentația principală
├── requirements.txt             # Dependențe Python
├── docs/
│   └── datasets/               # Descriere seturi de date, surse, diagrame
├── data/
│   ├── raw/                    # Date brute (imagini originale)
│   ├── processed/              # Date curățate și transformate
│   ├── train/                  # Set de instruire
│   │   ├── benign/            # Imagini leziuni benigne
│   │   └── malignant/         # Imagini leziuni maligne
│   ├── validation/             # Set de validare
│   │   ├── benign/
│   │   └── malignant/
│   └── test/                   # Set de testare
│       ├── benign/
│       └── malignant/
├── src/
│   ├── __init__.py
│   ├── preprocessing/          # Funcții pentru preprocesare imagini
│   │   ├── __init__.py
│   │   ├── image_processing.py
│   │   └── data_augmentation.py
│   ├── data_acquisition/       # Descărcare și organizare date
│   │   ├── __init__.py
│   │   └── download_dataset.py
│   ├── neural_network/         # Implementarea rețelei neuronale
│   │   ├── __init__.py
│   │   ├── model.py
│   │   ├── train.py
│   │   └── evaluate.py
│   └── utils/                  # Utilități generale
│       ├── __init__.py
│       └── helpers.py
├── config/                     # Fișiere de configurare
│   └── config.yaml
├── notebooks/                  # Jupyter notebooks pentru experimente
│   └── exploratory_analysis.ipynb
└── models/                     # Modele antrenate salvate
    └── .gitkeep
```

---

## 🔧 Instalare și Configurare

### Cerințe Sistem
- Python 3.12+
- GPU cu CUDA (recomandat pentru antrenare)

### Pași de Instalare

1. **Clonează repository-ul:**
```bash
git clone [URL_REPOSITORY]
cd Melanom_AI
```

2. **Creează un mediu virtual:**
```bash
python -m venv venv
.\venv\Scripts\activate  # Windows
```

3. **Instalează dependențele:**
```bash
pip install -r requirements.txt
```

---

## 📊 Setul de Date

### Sursa datelor
- **Dataset:** ISIC (International Skin Imaging Collaboration)
- **Tip:** Imagini dermatoscopice
- **Clase:** Benign, Malign (Melanom)

### Caracteristici
- **Format:** JPEG/PNG
- **Rezoluție:** Variabilă (se redimensionează la 224x224)
- **Număr imagini:** ~10,000+ (în funcție de subset)

---

## 🧠 Arhitectura Modelului

Modelul utilizează o arhitectură **CNN** (Convolutional Neural Network) bazată pe:
- Transfer Learning cu modele pre-antrenate (VGG16/ResNet50/EfficientNet)
- Layers de convoluție pentru extragerea caracteristicilor
- Batch Normalization și Dropout pentru regularizare
- Clasificator final cu activare sigmoid pentru clasificare binară

---

## 📈 Metrici de Evaluare

- **Accuracy** - Acuratețea generală
- **Precision** - Precizia (minimizarea fals pozitivelor)
- **Recall/Sensitivity** - Sensibilitatea (minimizarea fals negativelor - crucial în diagnostic medical)
- **F1-Score** - Media armonică
- **AUC-ROC** - Aria sub curba ROC

---

## 🚀 Utilizare

### Antrenare model:
```bash
python src/neural_network/train.py
```

### Evaluare model:
```bash
python src/neural_network/evaluate.py
```

### Predicție pe imagini noi:
```bash
python src/neural_network/predict.py --image path/to/image.jpg
```

---

## 📝 Etape Proiect

- [x] Etapa 1: Definirea problemei și obiectivelor
- [x] Etapa 2: Studiul literaturii și alegerea arhitecturii
- [x] Etapa 3: Analiza și pregătirea setului de date
- [ ] Etapa 4: Implementarea și antrenarea modelului
- [ ] Etapa 5: Evaluarea și optimizarea modelului
- [ ] Etapa 6: Documentație finală și prezentare

---

## 📚 Referințe

- ISIC Archive: https://www.isic-archive.com/
- Keras Documentation: https://keras.io/
- TensorFlow: https://www.tensorflow.org/

---

## 📄 Licență

Acest proiect este realizat în scop educațional pentru disciplina Rețele Neuronale.

---

**© 2024 Dumitru Claudia Ștefania - POLITEHNICA București**
