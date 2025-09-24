# Reply Classification API

This API classifies email replies into `positive`, `negative`, or `neutral` categories using a fine-tuned **DistilBERT** model.

## Project Structure

```
├── app.py                               # Flask API application
├── notebook.ipynb                       # ML pipeline notebook
├── answers.md                          # Reasoning answers
├── best_model.pkl                      # Trained ensemble model
├── vectorizer.pkl                      # TF-IDF vectorizer
├── cleaned_dataset.csv                 # Processed dataset
├── reply_classification_dataset.csv    # Original dataset
├── requirements.txt                    # Python dependencies
├── Dockerfile                          # Docker configuration
└── README.md                          # This file
```

## Model Performance

- **Best Model**: Ensemble (Logistic Regression + SVM + Naive Bayes)
- **Accuracy**: 95.38%
- **F1 Score**: 95.44%

### Model Comparison
| Model | Accuracy | F1 Score |
|-------|----------|----------|
| Logistic Regression | 95.38% | 95.44% |
| Random Forest | 89.23% | 89.29% |
| Ensemble | 95.38% | 95.44% |

## API Usage

### Starting the Server
```bash
pip install -r requirements.txt
python app.py
```

Server runs on `http://localhost:5000`

### API Endpoints

#### POST /predict
Classify a reply text.

**Request:**
```json
{
    "text": "Looking forward to the demo!"
}
```

**Response:**
```json
{
    "label": "positive",
    "confidence": 0.87
}
```

**Response:**
```json
{
    "status": "healthy"
}
```

### Example Usage
```bash
curl -X POST http://localhost:5000/predict \
     -H "Content-Type: application/json" \
     -d '{"text": "I am excited to see the demo!"}'
```

## Docker Deployment

Build and run with Docker:
```bash
docker build -t reply-classifier .
docker run -p 5000:5000 reply-classifier
```

