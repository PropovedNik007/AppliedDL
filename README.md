# Applied Deep Learning Project - Remote-Controlled RC Car with Real-Time Semantic Segmentation in Indoor Environment

## Overview and Goals

This project aims to build a **real-time semantic segmentation system** for a **self-driven RC car**. 
The main goal is to allow the RC car to autonomously drive by detecting and avoiding obstacles, tracking routes, and in the future, solving more complex tasks like object retrieval.

### Key Objectives:
1. **Real-time Semantic Segmentation**: Develop a lightweight segmentation model to distinguish between drivable surfaces and obstacles.
2. **Future Task Solving**: Expand the system to perform complex tasks like object retrieval and multi-step navigation using reinforcement learning.

---

## Project Approach

### 1. References to Scientific Papers

- **Fast-SCNN: Fast Semantic Segmentation Network**  
  This paper introduces a lightweight segmentation model that can achieve real-time performance, ideal for indoor environments and mobile applications like this project.

- **ENet: A Deep Neural Network Architecture for Real-Time Semantic Segmentation**  
  This model provides efficient segmentation with a focus on real-time applications, which is well-suited for indoor navigation tasks where precision and speed are critical.

- **PIDNet: A Real-time Semantic Segmentation Network Inspired by PID Controllers**  
  This paper introduces a segmentation model inspired by PID controllers, which could be an interesting alternative for real-time applications like autonomous navigation.

- **Lightweight Real-time Semantic Segmentation Network with Efficient Transformer and CNN**  
  This paper introduces a LETNet model that combines transformer and CNN architectures for efficient and real-time semantic segmentation, which could be beneficial for this project.

### 2. Decision of a Topic

**Topic**: Real-Time Semantic Segmentation for Navigation**  
The model will process the RC car’s live camera feed, identifying drivable areas and obstacles (such as furniture or walls).

### 3. Type of Project

**Bring your own method**
This project will build upon existing architectures while incorporating improvements from transformer-based models. The focus will be on optimizing the architecture to improve speed without sacrificing accuracy. Pruning and quantization will be used for further optimization, ensuring that the model can run in real-time.

## 4. Written Summary

### a. Short Description of the Project Idea and Approach

The goal of the project is to build a **real-time semantic segmentation model** that delivers high segmentation accuracy while maintaining low latency, suitable for real-time applications such as video processing and autonomous systems.
Lightweight backbones like **MobileNet** or **EfficientNet** will be used to improve inference speed. The model will be trained on indoor datasets to recognize common room elements like floors, walls, and furniture, enabling an RC car to navigate autonomously in an indoor environment.
Preferably to deploy the model on a **Raspberry Pi** for real-time inference, but in case of computational limitations, model inference can be offloaded to a remote laptop. 
Future steps probably outside the scope of this project are integrating reinforcement learning for more advanced tasks like object retrieval and dynamic obstacle avoidance.

### b. Description of the dataset

- **Dataset**: Since the RC car will be navigating indoor mostly, publicly available datasets like **ADE20K**, **SUN RGB-D** or **NYU Depth v2** (which contain annotated indoor scenes) will be appropriate for training the model. 
 These datasets have labeled indoor environments, including furniture and other common household objects, which are relevant to this project. 
 Also **COCO** and **Pascal VOC** are common public datasets for segmentation.
- **Optional**: Collecting my own dataset by capturing images and annotating them with segmentation masks using tools like **LabelMe** or **VGG Image Annotator**. In case of ramps, stairs, or other specific features in the room, custom annotations will be necessary.
 

### c. Work-Breakdown Structure

| **Task**                         | **Time Estimate** |
| --------------------------------- |-------------------|
| Literature Review                 | 2-3 days          |
| Dataset Collection & Preprocessing| 2-5 days          |
| Model Architecture Design         | 4-5 days          |
| Model Training & Fine-Tuning       | 7-10 days         |
| Hardware Setup (RC Car & Wi-Fi)   | 3-4 days          |
| Real-Time Integration (Laptop & RC Car) | 5-7 days          |
| Testing on RC Car (Indoor Setup)  | 3-4 days          |
| Model Optimization for Real-Time  | 3-4 days          |
| Future Task Integration           | 5-6 days          |
| Final Report and Presentation     | 2-3 days          |

## Future Expansion: Task-Solving RC Car

Once basic indoor navigation is achieved, the project can be expanded to include:
- **Object Detection & Retrieval**: Implement object detection to recognize and approach specific objects in the room. This will allow the car to perform tasks like retrieving objects.
- **Reinforcement Learning**: Integrate reinforcement learning for more advanced navigation tasks (e.g., navigating around dynamic obstacles or optimizing paths in a cluttered room).
- **Complex Task Solving**: The RC car could be tasked with finding and interacting with objects in the room, such as pushing or retrieving items.

