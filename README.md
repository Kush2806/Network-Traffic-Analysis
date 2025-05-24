# Network Traffic Analysis using Machine Learning

A comprehensive network traffic analysis system that combines computer vision and machine learning techniques for anomaly detection in network traffic. This project utilizes Intel's optimized libraries for enhanced performance and implements both traditional machine learning and deep learning approaches for robust anomaly detection.

## Project Overview

This project consists of two main components:
1. **Network Traffic Analysis**: Anomaly detection in network traffic using machine learning
2. **Computer Vision Component**: Green object detection using OpenCV

## Features

### Network Traffic Analysis
- Real-time network traffic monitoring and analysis
- Anomaly detection using ensemble methods (Isolation Forest + Random Forest)
- Deep learning-based anomaly detection using Autoencoders
- Optimized performance using Intel's libraries
- Comprehensive data visualization and analysis

### Computer Vision
- Real-time video processing
- Green object detection and tracking
- Frame-by-frame analysis
- Visual feedback and display

## Technical Architecture

### Data Processing Pipeline
1. **Data Collection**: Network traffic data captured using Wireshark
2. **Data Preprocessing**: Feature extraction and normalization
3. **Model Training**: Ensemble of traditional ML and deep learning models
4. **Anomaly Detection**: Real-time detection and classification
5. **Visualization**: Results display and analysis

### Model Architecture

#### Autoencoder Architecture
```
Input Layer → Encoding Layers → Bottleneck → Decoding Layers → Output Layer
- Input Layer: Raw features
- Encoding Layers: 64 → 32 neurons with ReLU
- Bottleneck: 10 neurons
- Decoding Layers: 32 → 64 neurons with ReLU
- Output Layer: Reconstruction with sigmoid activation
```

#### Ensemble Method
- **Isolation Forest**: Initial anomaly score estimation
  - Contamination: 0.0045
  - Random state: 42
- **Random Forest Classifier**: Refinement of anomaly detection
  - Estimators: 100
  - Random state: 42

## Performance Optimization

### Intel Optimizations
1. **Intel Extension for TensorFlow**
   - Accelerated training and inference
   - oneDNN optimizations
   - Deep Learning Boost features

2. **Intel Distribution for Python**
   - Multi-core CPU optimization
   - Native tool integration
   - CPython compatibility

3. **Intel Extension for scikit-learn**
   - Up to 100x acceleration
   - Seamless scikit-learn integration
   - Multi-device support

## Dataset Structure

The network traffic dataset (`late.csv`) contains the following features:
- No.: Packet sequence number
- Time: Timestamp
- Source: Source IP address
- Destination: Destination IP address
- Protocol: Network protocol
- Length: Packet length
- Info: Additional packet information

## Installation

1. Clone the repository:
```bash
git clone https://github.com/yourusername/Network-Traffic-Analysis-using-Machine-learning.git
```

2. Install dependencies:
```bash
pip install -r requirements.txt
```

3. Enable Intel optimizations:
```bash
export TF_ENABLE_ONEDNN_OPTS=1
```

## Usage

### Network Traffic Analysis
```python
from anomalydetection import NetworkAnalyzer

analyzer = NetworkAnalyzer()
analyzer.train()
anomalies = analyzer.detect_anomalies()
```

### Computer Vision Component
```python
python main6.py
```

## Performance Comparison

The project demonstrates significant performance improvements when using Intel optimizations:
- Reduced training time
- Improved inference speed
- Better resource utilization

## Contributors

- [@navabhaarathi](https://github.com/nb0309)
- [@balasuriya](https://github.com/balasuriyaranganathan/balasuriyaranganathan)

## Acknowledgements

- [Computer Network Intrusion and Anomaly Detection](https://www.hindawi.com/journals/misy/2022/6576023/)
- [Intel Distribution for Python](https://www.intel.com/content/www/us/en/developer/tools/oneapi/distribution-for-python.html)
- [Intel oneAPI](https://www.oneapi.io/)
- [Wireshark](https://www.wireshark.org/)

## License

This project is licensed under the MIT License - see the LICENSE file for details.
