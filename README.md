# Standalone Smart Hajj Earbud Assistant

An integrated, wearable Edge-AI assistive device designed to enhance the safety, health tracking, and communication of pilgrims during Hajj. This project directly contributes to the digital transformation goals of **Saudi Vision 2030** by leveraging digital technologies to provide a safer and more efficient mass gathering experience.

---

## Project Overview
During Hajj, millions of pilgrims face significant health, physical, and language communication challenges. This project proposes a **Standalone Smart Earbud** that integrates automated translation, continuous vital signs monitoring, and real-time location tracking. 

The earbud serves as a critical link between pilgrims and medical/campaign supervisors. In emergency situations, it automatically transmits the pilgrim's precise location and health metrics via cellular networks for rapid medical intervention.

---

##  Key Features & Functionalities
* **Keyword Spotting (KWS) System:** Continuous background audio processing to detect predefined keywords and automatically activate the translation system.
* **Automated Audio Translation:** Facilitates real-time verbal communication between pilgrims and Arabic speakers (including medical teams and supervisors) to overcome language barriers.
* **Continuous Health Monitoring:**  monitoring of vital signs including heart rate, oxygen levels ($SpO_2$), and body temperature.
* **Intelligent Emergency Response (SOS):** * Manual activation via a physical SOS button.
  * Automatic activation if a critical health condition is detected.
  * Sends immediate SMS alerts containing GPS coordinates and medical data to the supervisor.

---

##  Hardware & System Architecture

### System Components
* **Processing Unit:** ESP32-S3 Microcontroller (ideal for low-power Edge AI applications).
* **Inputs:** Microphone (Voice Input), Vital Signs Sensors (PPG/Temperature), and a physical SOS Button.
* **Outputs & Communication:** Audio Output (Earbud speaker), GSM/GPS integrated Module (for sending SMS data), and location tracking.

### System Flowchart
The earbud initializes by receiving setup parameters (selected translation language and supervisor contact details) via SMS. Once active, it continuously loops through vital signs monitoring and KWS scanning until turned off.
<img width="663" height="503" alt="image" src="https://github.com/user-attachments/assets/fb577d3c-6a01-4faf-9a39-59805b4ceb5a" />

---

##  Software & TinyML Implementation
The core machine learning component (Keyword Spotting System) was designed following modern **TinyML** practices to run efficiently on resource-constrained hardware:
### Model Architecture
Here is the neural network architecture designed for the Keyword Spotting (KWS) system:
<img width="1132" height="1656" alt="Screenshot 2026-06-20 at 9 25 08 PM" src="https://github.com/user-attachments/assets/e295b666-776c-4c9b-a603-58773ff2f3e8" />

* **Development Environment:** Developed using Google Colab with GPU acceleration for highly efficient training.
* **Data Augmentation:** Audio preprocessing techniques, including noise injection and echo simulation, were applied to training datasets to replicate real-world crowd conditions during Hajj.
* **Model Deployment:** The trained neural network was optimized and converted into **TensorFlow Lite (TF Lite) format** to fit onto the microcontroller's flash memory.

---

## Results & Artifacts

* **Model Performance:** The trained KWS model achieved high accuracy and robust convergence during training and validation, as demonstrated by the evaluation metrics (Confusion Matrix and Loss/Accuracy curves).
<img width="1903" height="1059" alt="Screenshot 2026-06-04 154503" src="https://github.com/user-attachments/assets/d3d602de-998e-4cce-b252-f398d3e8670a" />
<img width="1920" height="1080" alt="Screenshot 2026-06-04 154646" src="https://github.com/user-attachments/assets/7178f7fb-d992-40b1-a88b-4b5a9bd30fdc" />


### 📂 Project Documentation
* **Project Presentation:** [Download/View Presentation PDF](presentation.pdf)
  
* **Project Poster:** [Download/View Poster PDF](poster.pdf)
  
* **Video Demonstration:**
  https://drive.google.com/file/d/1hmwNn0QASMDEc8QMWpB2e99zIvRB3RI-/view?usp=drivesdk

---

## 👥 Project Team
* **Developers:** Albatol A. Almalki, Raneem N. Almalki, Abeer O. Alqurashi, Manar M. Alosaimi, Ahlam A. Alwathinani, Ruba J. Alharthi.
* **Supervisor:** Dr. Shaima Elnazer.
* **Institution:** Taif University, College of Computers and Information Technology, Department of Computer Engineering.
* **Date:** May 2026.
