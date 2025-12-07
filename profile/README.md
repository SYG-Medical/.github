# AIVertigoLab - AI-Powered Vertigo Diagnosis and Management System

AIVertigoLab is a comprehensive platform for the diagnosis and management of vertigo (dizziness) and balance disorders, developed by SYG Medical. This system integrates artificial intelligence with medical devices to provide advanced solutions for vertigo diagnosis and treatment.

## Mission

To develop intelligent, data-driven solutions that enhance the diagnosis, treatment, and management of vertigo and balance disorders through the integration of medical technology and artificial intelligence.

## Project Architecture

AIVertigoLab consists of several interconnected components working together to create a complete vertigo diagnosis and management ecosystem:

### 1. Medical Management System (Backend + Frontend)

**Purpose**: Central management system for vertigo diagnosis and treatment centers.

**Key Features**:
- **User & Role Management**: Multi-role system (Admin, Center Manager, Representative, Doctor, External Doctor)
- **Doctor & Representative Management**: Doctor registration, certification, and hospital representation
- **Hospital Management**: Hospital types, groups, and contact information management
- **Device Management (RMS/VNG)**: Central management of vertigo diagnosis devices (Rotary Chair System, Videonystagmography)
- **License & Maintenance Tracking**: Device licensing and maintenance schedule management
- **KVKK Compliance**: Personal data protection and consent management (GDPR equivalent)
- **Request & Appointment Management**: External doctor requests and center appointments
- **Reporting & Analytics**: Treatment statistics, device usage, and performance metrics

**Technologies Used**:
- **Backend**: Node.js, Express, MySQL, NATS messaging
- **Frontend**: React, Vite, CoreUI, Chart.js, Firebase
- **Authentication**: JWT, Firebase Admin
- **Communication**: Nodemailer, NetGSM SMS integration

---

### 2. Artificial Intelligence Module (yapayZeka)

**Purpose**: AI-powered video analysis for automated vertigo diagnosis.

**Key Features**:
- **Video Processing**: Automated analysis of eye movement videos from RMS/VNG devices
- **Pupil & Iris Tracking**: Computer vision-based tracking of ocular parameters
- **Nystagmus Detection**: AI detection of nystagmus patterns (horizontal, vertical, torsional)
- **SAM2 Model Integration**: Segment Anything Model 2 for advanced medical image segmentation
- **YOLO Object Detection**: Real-time object detection in medical videos
- **CNN-GRU Models**: Convolutional Neural Networks with Gated Recurrent Units for time-series analysis
- **Web Interface**: Flask-based web application for video upload and analysis

**Technologies Used**:
- **AI/ML**: PyTorch, OpenCV, SAM2, YOLO
- **Backend**: Flask (Python)
- **Frontend**: HTML, CSS, JavaScript
- **Video Processing**: FFmpeg, OpenCV video analysis

---

### 3. MQTT Broker

**Purpose**: MQTT-based message broker enabling real-time communication with RMS (Rotary Chair System) medical devices.

**Technologies Used**:
- **MQTT Protocol**: Lightweight publish-subscribe messaging
- **Integration**: Connects medical devices with the central management system

---

### 4. WebSocket Service

**Purpose**: Real-time communication service for live data streaming from medical devices.

**Technologies Used**:
- **WebSocket Protocol**: Bidirectional real-time communication
- **NATS Integration**: High-performance messaging system
- **Database**: MySQL for persistent data storage

---

### 5. Database System (veritabani)

**Purpose**: Comprehensive database for patient records, device data, and medical metrics.

**Features**:
- **Patient Records**: Medical history and treatment data
- **Device Data**: RMS and VNG device measurements
- **Appointment Scheduling**: Center and doctor appointments
- **Reporting Data**: Treatment outcomes and statistics
- **Regular Backups**: Scheduled database dumps (SQL format)

---

## Technical Stack

| Component          | Technologies                                                                 |
|--------------------|------------------------------------------------------------------------------|
| **Backend**        | Node.js, Express, MySQL, NATS, JWT, Firebase                                |
| **Frontend**       | React, Vite, CoreUI, Chart.js, Bootstrap, i18next                            |
| **Artificial Intelligence** | PyTorch, OpenCV, SAM2, YOLO, CNN-GRU models, Flask                   |
| **Messaging**      | MQTT, WebSocket, NATS                                                           |
| **DevOps**         | Docker, Git, Nodemon, ESLint                                                     |

---

## Key Features

1. **Integrated Medical Device Management**: Support for RMS (Rotary Chair System) and VNG (Videonystagmography) devices
2. **AI-Powered Diagnosis**: Automated analysis of vertigo using computer vision and deep learning
3. **Centralized Patient Management**: Comprehensive patient records and treatment history
4. **Real-time Data Streaming**: Live monitoring of vertigo tests and measurements
5. **Compliance & Security**: KVKK/GDPR compliance for patient data protection
6. **Multi-location Support**: Manage multiple diagnosis centers from a single platform

---

## Documentation

- **Backend API**: See `backend/README.md` for detailed API documentation
- **Frontend**: See `frontend/README.md` for React application details
- **AI Models**: See `yapayZeka/` directory for model training and inference code
- **Device Integration**: See `mqttBroker/` and `websocket/` directories for device communication protocols

---

## Contributing

We welcome contributions from the medical and technology communities. Please follow our contributing guidelines when submitting pull requests.

---

## Location

Istanbul, Turkey (UTC+3)
