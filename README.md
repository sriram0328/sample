# PlantDocBot: AI Plant Disease Diagnosis via Chat and Image Upload

An AI-powered chatbot that allows users (especially farmers and gardeners) to upload images of plant leaves or describe symptoms via text, and receive accurate plant disease diagnosis and treatment recommendations using computer vision and natural language processing techniques.

##  Overview

PlantDocBot combines the power of computer vision and NLP to provide an interactive tool capable of diagnosing common plant diseases from photos or text messages in real-time. The system processes both image uploads and symptom descriptions to deliver accurate disease identification and treatment recommendations.

##  Objective

To develop an AI-powered chatbot that enables:
- Image upload of plant leaves for disease detection
- Text-based symptom description and diagnosis
- Real-time disease identification and treatment recommendations
- Integration of image processing and natural language processing techniques

##  Key Features

- **Dual Input Modes**: Upload plant images OR describe symptoms via text
- **Image-Based Disease Detection**: CNN models (ResNet/MobileNet) trained on 50,000+ annotated plant leaf images
- **Text-Based Symptom Analysis**: BERT/GPT-based NLP for interpreting symptom descriptions
- **Treatment Recommendations**: Comprehensive cure methods and preventive measures
- **Interactive Chatbot**: Conversational AI for seamless user interaction
- **Real-time Diagnosis**: Instant disease identification with confidence scores

## 🏗️ Project Structure

```
PlantDocBot/
├── backend/
│   ├── app.py                              # Flask/FastAPI main application
│   ├── requirements.txt                     # Python dependencies
│   ├── plantdoc_cnn.pth                    # Trained CNN model
│   ├── label_encoder.pkl                    # Disease label encoder
│   ├── plant_disease_captions.parquet      # Disease information database
│   └── plant_disease_text_model/           # NLP model directory
│       ├── model.safetensors               # Fine-tuned BERT model
│       ├── config.json                      # Model configuration
│       ├── tokenizer.json                   # Tokenizer
│       ├── tokenizer_config.json            # Tokenizer configuration
│       ├── special_tokens_map.json          # Special tokens mapping
│       └── vocab.txt                        # Vocabulary file
│
├── frontend/
│   ├── index.html                           # Main HTML page
│   └── src/
│       ├── main.jsx                         # React entry point
│       └── App.jsx                          # Main App component
│
├── PlantDoc.ipynb                           # Model training & analysis notebook
├── .gitignore
└── LICENSE
```

## Datasets Used

1. **PlantVillage Dataset**: Open-source dataset with 50,000+ annotated plant leaf images for disease classification
2. **PlantDoc Dataset**: Real-world noisy images available on Kaggle for robust model training
3. **Text Corpus**: Plant symptom descriptions collected from agricultural forums, blogs, and research papers

## 🛠️ Technology Stack

### Backend
- **Framework**: Flask/FastAPI
- **Deep Learning**: TensorFlow/PyTorch
- **Image Processing**: OpenCV, PIL
- **NLP**: HuggingFace Transformers (BERT)
- **Model Format**: SafeTensors

### Frontend
- **Framework**: React.js
- **Language**: JSX/JavaScript
- **Build Tool**: Vite/Webpack

### Machine Learning
- **Vision Models**: ResNet, MobileNet (CNN architectures)
- **NLP Models**: BERT-based transformer for text classification
- **Model Serialization**: PyTorch (.pth), SafeTensors

## 🚀 Getting Started

### Prerequisites

- Python 3.8+
- Node.js 14+
- npm or yarn
- CUDA-capable GPU (optional, for faster inference)

### Installation

#### 1. Clone the Repository

```bash
git clone https://github.com/springboardmentor123g/PlantDocBotProject.git
cd PlantDocBotProject
git checkout Intern-SriramRamanadham
```

#### 2. Backend Setup

```bash
cd backend

# Create virtual environment
python -m venv venv

# Activate virtual environment
# Windows:
venv\Scripts\activate
# macOS/Linux:
source venv/bin/activate

# Install dependencies
pip install -r requirements.txt

# Start the backend server
python app.py
```

Backend will be available at `http://localhost:5000`

#### 3. Frontend Setup

```bash
cd frontend

# Install dependencies
npm install

# Start development server
npm run dev
```

Frontend will be available at `http://localhost:3000`

## 📱 System Modules

### 1. Dataset Collection and Preprocessing
- Image dataset cleaning and augmentation
- NLP corpus preparation
- Training/validation data splits

### 2. Image-based Plant Disease Detection
- CNN model training (ResNet/MobileNet)
- Image preprocessing pipeline
- Disease classification from leaf images

### 3. Symptom-based Text Diagnosis Chatbot
- BERT-based NLP model for symptom understanding
- Text classification and entity recognition
- Conversational response generation

### 4. Recommendation System
- Disease-to-treatment mapping
- Preventive measures database
- Confidence-based recommendations

### 5. User Interface
- Dual-mode input (image + text)
- Chat-based interaction
- Image upload mechanism
- Results visualization

### 6. Integration & Deployment
- Backend API endpoints
- Frontend-backend communication
- Model serving and inference
