# 🌿 AI Plant Disease Detection

A web-based application that uses artificial intelligence to detect diseases in plants by analyzing images. Simply upload a photo of your plant, and the AI will identify whether it's healthy or detect any diseases present.

## ✨ Features

- **AI-Powered Detection**: Uses TensorFlow/Keras deep learning model for accurate disease classification
- **Drag-and-Drop Upload**: Intuitive image upload with drag-and-drop support and preview
- **Real-time Analysis**: Get instant predictions with confidence scores
- **Disease Information**: Displays detailed information about detected diseases including:
  - Symptom descriptions
  - Prevention and treatment tips
  - Healthy plant care guidelines
- **Responsive Design**: Beautiful modern UI that works on desktop and mobile devices
- **Beautiful UI**: Modern blue/purple gradient theme with smooth animations

## 🎯 Supported Plant Diseases

Currently the model detects:
- **Tomato Early Blight** - Fungal disease with brown spots and yellow halos
- **Tomato Healthy** - Healthy plant status

## 🚀 Quick Start

### Prerequisites
- Python 3.10+
- pip (Python package manager)

### Installation

1. **Clone the repository**
   ```bash
   git clone https://github.com/Ankit-HubNation/plant-disease-detection.git
   cd plant-disease-detection
   ```

2. **Create virtual environment**
   ```bash
   python -m venv venv310
   ```

3. **Activate virtual environment**
   - On Windows:
     ```bash
     venv310\Scripts\activate
     ```
   - On macOS/Linux:
     ```bash
     source venv310/bin/activate
     ```

4. **Install dependencies**
   ```bash
   pip install -r requirements.txt
   ```

5. **Run the application**
   ```bash
   python app.py
   ```

6. **Open in browser**
   - Navigate to: `http://127.0.0.1:5000`

## 📁 Project Structure

```
plant-disease-detection/
├── app.py                 # Flask application main file
├── train.py              # Model training script
├── requirements.txt      # Python dependencies
├── README.md             # This file
├── dataset/              # Training and test datasets
│   ├── train/           # Training images
│   │   ├── Tomato_Early_blight/
│   │   └── Tomato_healthy/
│   └── test/            # Test images
├── model/               # Pre-trained model
│   └── plant_model.keras
├── static/              # Static files
│   ├── style.css        # Stylesheet
│   └── uploads/         # Uploaded images storage
└── templates/           # HTML templates
    ├── index.html       # Upload page
    └── result.html      # Results page
```

## 🛠️ Technologies Used

- **Backend**: Flask (Python web framework)
- **ML/AI**: TensorFlow, Keras (Deep Learning)
- **Image Processing**: OpenCV, NumPy
- **Frontend**: HTML5, CSS3, JavaScript
- **Image Formats**: JPG, PNG, WEBP

## 📊 Model Details

- **Architecture**: Convolutional Neural Network (CNN)
- **Framework**: Keras/TensorFlow
- **Input Size**: 128x128 pixels
- **Output**: Classification with confidence score
- **File**: `model/plant_model.keras`

## 🎨 UI Features

### Home Page
- Drag-and-drop image upload area
- Image preview before analysis
- File selection with browsing
- Supported format information

### Results Page
- Uploaded image display
- Disease/condition classification
- Confidence score with visual progress bar
- Detailed disease information
- Prevention and care tips
- Option to analyze another plant

## 📖 How to Use

1. **Upload Image**
   - Drag and drop an image of your plant, or
   - Click "Browse Files" to select an image
   - Preview appears before submission

2. **Analyze**
   - Click "Detect Disease" button
   - Wait for AI analysis (usually 1-2 seconds)

3. **View Results**
   - See the detected condition
   - Check confidence score
   - Read disease information and prevention tips
   - Click "Analyze Another Plant" to continue

## 🔄 Training the Model

To train your own model with custom dataset:

```bash
python train.py
```

This will:
- Load images from `dataset/train/`
- Train a CNN model
- Save the model as `plant_model.keras`

## 📋 Requirements

See `requirements.txt` for full list. Key packages:
- flask==3.1.3
- tensorflow>=2.0
- keras>=3.0
- opencv-python
- numpy
- Pillow

## 🐛 Troubleshooting

**Port 5000 already in use**
- Change the port in `app.py`: `app.run(debug=True, port=5001)`

**Model loading errors**
- Ensure `model/plant_model.keras` exists
- Check TensorFlow version compatibility

**Image upload issues**
- Ensure `static/uploads/` directory exists
- Check file permissions

## 📝 API Endpoints

- `GET /` - Home page with upload form
- `POST /predict` - Process image and return prediction
  - Returns: `result.html` with prediction and confidence score

## 🚀 Future Enhancements

- [ ] Support for more plant types (wheat, rice, potato, etc.)
- [ ] Batch image processing
- [ ] Export results as PDF
- [ ] Integration with weather data for better recommendations
- [ ] Mobile app version
- [ ] Multi-language support
- [ ] User accounts and history tracking

## 📄 License

This project is open source and available under the MIT License.

## 🤝 Contributing

Contributions are welcome! Please feel free to submit a Pull Request.

## 👨‍💻 Author

- **Ankit** - Initial work

## 📞 Support

For issues, questions, or suggestions, please open an issue in the GitHub repository.

## 🙏 Acknowledgments

- TensorFlow/Keras team for the amazing ML framework
- Flask community for the web framework
- All contributors and testers

---

**Happy Plant Detection! 🌿✨**
