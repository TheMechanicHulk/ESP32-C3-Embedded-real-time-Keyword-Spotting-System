# ESP32-C3 Embedded Keyword Spotting System with Quantized TFLite Model

## Overview
This project demonstrates developing a keyword-spotting system using a Convolutional Neural Network (CNN) model deployed on an ESP32-C3 microcontroller. The CNN model was trained using Keras, quantized to TensorFlow Lite (TFLite) format, and integrated with an I2S microphone for real-time keyword recognition. The system can identify specific spoken words with an accuracy of 93%, even in resource-constrained environments.

## Features
- **Keyword Spotting**: Real-time detection of specific spoken keywords with a CNN model.
- **Model Accuracy**: Achieved 93% accuracy using a custom-trained CNN model for keyword recognition.
- **Quantized Model**: Optimized the model by converting it into TFLite format for deployment on the ESP32-C3.
- **Real-Time Inference**: The ESP32-C3 performs real-time keyword spotting by interfacing with an I2S microphone.
- **Low-Power Embedded Solution**: Designed for resource-limited environments while maintaining performance.

## Workflow
1. **Model Training**: 
    - Built and trained a CNN model using the Keras framework on a dataset of voice recordings.
    - Fine-tuned the model for better accuracy in recognizing specific keywords.
2. **Model Quantization**:
    - Quantized the trained model using TensorFlow Lite for efficient execution on the ESP32-C3’s limited hardware.
3. **Deployment on ESP32-C3**:
    - Deployed the TFLite model onto the ESP32-C3 System-on-Chip (SoC).
    - Integrated the I2S microphone for real-time audio input and keyword detection.
4. **Real-Time Keyword Spotting**:
    - The ESP32-C3 performs inference on the input audio data in real-time, identifying keywords based on the trained model.

## Technologies Used
- **Keras**: Used for developing and training the CNN model for keyword spotting.
- **TensorFlow Lite**: Employed for model quantization and optimizing it for embedded deployment.
- **ESP32-C3**: The target SoC for real-time keyword recognition, interfacing with an I2S microphone.
- **I2S Microphone**: Used to capture real-time audio data for keyword spotting.
- **PlatformIO**: For writing and deploying the embedded code onto ESP32-C3.

## How to Run the Project
1. **Install PlatformIO**: Set up PlatformIO as the IDE for building and deploying code to the ESP32-C3.
2. **Clone the Repository**:
    ```bash
    git clone https://github.com/TheMechanicHulk/ESP32-C3-Keyword-Spotting.git
    ```
3. **Load TFLite Model**: Download and deploy the quantized TFLite model to the ESP32-C3 flash memory.
4. **Connect I2S Microphone**: Wire up the I2S microphone to the ESP32-C3 pins as per the schematic provided in the `docs/` folder.
5. **Build & Deploy**: Compile and upload the code to the ESP32-C3 using PlatformIO.
6. **Run**: Power the ESP32-C3, and the system will recognize keywords from the audio input in real time.

## File Structure
- `model/`: Contains the trained and quantized CNN model files.
- `src/`: Contains the source code for the ESP32-C3 that loads the TFLite model and performs keyword spotting.
- `docs/`: Contains wiring diagrams and documentation on hardware setup and interfacing.
- `test/`: Test scripts to evaluate model performance on ESP32-C3.

## Hardware Setup
- **ESP32-C3 SoC**
- **I2S Microphone**: For real-time voice input
- **OLED Display** (Optional): This visualizes keyword detection results.

## Future Improvements
- **Noise Filtering**: Improve robustness by integrating noise filtering techniques for better accuracy in noisy environments.
- **Additional Keyword Support**: Train the model to recognize additional keywords more precisely.
- **Wake Word Detection**: Implement wake word detection to activate the system only when a specific keyword is detected.

## Acknowledgements
Special thanks to the TensorFlow and Keras communities for their resources and support, as well as Espressif for the ESP32 platform.


