# 🤖 Object Detection with AWS Rekognition

> Cloud AI / Grad Project — Python + boto3 + AWS Rekognition

---

## 📌 Overview

This project uses **AWS Rekognition** and **Python (boto3)** to perform object detection on images. It draws bounding boxes around detected objects with confidence-scored labels using the Pillow library. The project also includes a fun **"Hot Dog / Not Hot Dog"** food classifier inspired by the Silicon Valley TV show.

---

## 🛠️ Technologies Used

- **AWS Rekognition** — Cloud-based computer vision service
- **Python** — Core programming language
- **boto3** — AWS SDK for Python
- **Pillow (PIL)** — Image processing and annotation
- **CSV** — AWS credentials management

---

## 🏗️ Project Components

### 1. Object Detection (`object-detection.py`)
Detects and labels objects in a local image file using AWS Rekognition's `detect_labels` API. Draws bounding boxes around each detected object with the label name and confidence score.

### 2. Food Classifier (`seefood.py`)
Classifies images from a URL as:
- 🌭 **Hot Dog** — if Rekognition detects a hot dog
- 🍕 **Not Hot Dog** — if food is detected but not a hot dog
- ❌ **Not Food** — if no food is detected at all

---

## ⚙️ How It Works

```
Input Image (URL or local file)
        │
        ▼
AWS Rekognition detect_labels API
        │
        ▼
Response: Labels + Confidence Scores + Bounding Boxes
        │
        ▼
Pillow draws bounding boxes + label text on image
        │
        ▼
Output: Annotated image displayed
```

---

## 📁 Files

| File | Description |
|------|-------------|
| `object-detection.py` | Main object detection script with bounding box rendering |
| `seefood.py` | Hot Dog / Not Hot Dog food classifier |
| `people.jpeg` | Sample input image for object detection |
| `output1.png` | Sample output — annotated image with bounding boxes |
| `output2.png` | Sample output — second annotated result |
| `arial.ttf` | Font file used for label rendering |

---

## 🚀 Setup & Usage

### Prerequisites
```bash
pip install boto3 pillow
```

### AWS Credentials
Configure your AWS credentials either via:
```bash
aws configure
```
Or by placing them in `credentials.csv` (format: `username, password, access_key_id, secret_access_key, console_link`)

### Run Object Detection
```bash
python object-detection.py
```

### Run Food Classifier
```bash
python seefood.py
```
Modify the `img` variable in `seefood.py` to point to your image URL or local file.

---

## 🔍 Sample Output

The script detects objects like **Person, Clothing, Outdoors** etc. and draws color-coded bounding boxes with labels directly on the image.

---

## 📚 Key Concepts Demonstrated

- ✅ AWS Rekognition `detect_labels` API
- ✅ boto3 — AWS SDK for Python
- ✅ Bounding box rendering with Pillow
- ✅ Image processing and annotation
- ✅ Cloud AI service integration
- ✅ Confidence threshold filtering
- ✅ Computer vision (object detection)

---

## 📄 Related Publication

This project is linked to a published research paper on AI-based environmental detection:

**Air Pollution Detection using ResNet-50**
*IEEE — International Conference on Environmental Science & Computer Science (Feb 2023)*

---

## 👩‍💻 Author

**Jyothika Vempatapu**
M.S. Cybersecurity — University of South Florida
[LinkedIn](https://linkedin.com/in/jyothika--v) • [GitHub](https://github.com/jyothikavempatapu)
