# MobileBarcodeExpiryAnnotator

AI-augmented mobile app for barcode and expiry date annotation using TensorFlow Lite.

## Overview

MobileBarcodeExpiryAnnotator is a cross-platform mobile application built with React Native that leverages TensorFlow Lite for on-device machine learning inference. The app enables users to capture, detect, and annotate barcodes and expiry dates efficiently on their mobile devices.

## Architecture Overview

This project combines React Native's cross-platform capabilities with TensorFlow Lite's high-performance on-device inference to create a scalable, maintainable, and user-friendly AI-powered annotation application.

### Key Components

#### React Native for Cross-Platform UI
- **Screens & Navigation:** Develop app screens, camera interface, and user navigation flows
- **Annotation Overlays:** Create interactive annotation overlays for bounding boxes and text displays
- **User Inputs:** Handle user interactions for accepting, adjusting, or correcting AI-generated annotations
- **Cross-Platform Deployment:** Build once and deploy on both Android and iOS, accelerating development and maintenance cycles

#### TensorFlow Lite Integration
- **On-Device Inference:** Run YOLOv8 barcode detection and OCR models natively on-device for privacy and reduced latency
- **Native Module Bridges:** Integrate TensorFlow Lite via community libraries or custom native modules
- **Android:** Java/Kotlin implementation for efficient model execution
- **iOS:** Swift/Objective-C implementation for seamless integration with Apple's ecosystem
- **Model Optimization:** Deploy quantized and optimized models for mobile hardware constraints

#### Camera Functionality
- **Camera Access:** Integrate React Native Camera or React Native Vision Camera libraries
- **Real-time Capture:** Capture photos and video frames from device cameras
- **Frame Processing:** Feed captured images to ML models for inference
- **Viewfinder:** Display camera feed with live detection overlays

#### Annotation Interaction
- **SVG/Canvas Overlays:** Create interactive visual elements for bounding boxes and detected elements
- **Text Input:** Allow users to enter or correct text for detected values
- **Adjustment Tools:** Enable users to refine bounding box positions and dimensions
- **Smooth UX:** Optimize for mobile touch interactions with responsive feedback

#### Storage and Sync
- **Local Storage:** Use React Native AsyncStorage for lightweight annotation data persistence
- **SQLite Integration:** For more complex queries and structured data storage
- **Backend Sync:** Optional synchronization with backend servers for:
  - Centralized annotation review
  - Model retraining with collected data
  - Incremental model improvements over time
- **Offline Capability:** Full functionality without network connectivity

#### Performance Optimization
- **Native Bridge Optimization:** Minimize overhead in React Native-to-Native communication
- **TensorFlow Lite Performance Tuning:**
  - Leverage GPU/NNAPI acceleration where available
  - Profile and optimize model inference latency
  - Balance model accuracy with inference speed
- **Resource Management:** Efficient memory and battery usage
- **Threading:** Offload heavy computation from UI thread to prevent jank

## Technology Stack

- **Frontend:** React Native
- **ML Framework:** TensorFlow Lite
- **Computer Vision:** YOLOv8 (barcode detection), OCR models
- **Camera:** React Native Camera / React Native Vision Camera
- **Storage:** AsyncStorage, SQLite
- **State Management:** [To be determined based on project scale]
- **Native Development:** Java/Kotlin (Android), Swift/Objective-C (iOS)

## Project Goals

1. Enable accurate barcode detection using YOLOv8 on mobile devices
2. Extract and recognize expiry dates through on-device OCR
3. Provide seamless user experience for annotation correction
4. Support offline operation with optional cloud synchronization
5. Build a foundation for continuous model improvement through user feedback
