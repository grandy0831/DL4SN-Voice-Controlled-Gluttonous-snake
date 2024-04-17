# Voice-Controlled Gluttonous Snake

**Author:** Guandi Chen

**GitHub Repository:** [https://github.com/grandy0831/DL4SN-Voice-Controlled-Gluttonous-snake](https://github.com/grandy0831/DL4SN-Voice-Controlled-Gluttonous-snake)

**Edge Impulse Project:** [https://studio.edgeimpulse.com/studio/380405](https://studio.edgeimpulse.com/studio/380405)


## Introduction

This project aims to develop a voice-controlled system for the classic game Snake. With the rapid development of the Internet of Things (IoT) and smart home technologies, voice interaction is becoming an integral and efficient mode of everyday interaction. Inspired by trends in modern interactive technologies, this project explores the potential of voice recognition in game control by enabling directional commands such as "up," "down," "left," and "right" to manipulate game movements.

The game control system captures the player's voice commands through an integrated microphone, processes and recognizes them in real-time, and translates them into movement controls within the game. This interaction allows the player to seamlessly control the game using voice alone, without the need for physical controllers, creating a new gaming experience.

### Key Inspiration:
1. **Smart Assistants**: The everyday use of devices like Alexa and Google Home reflects the reliability and user-friendliness of voice-controlled systems.
2. **Voice Recognition in Apps**: Mobile applications utilizing voice commands are becoming commonplace, demonstrating the technology's versatility.
3. **Accessible Gaming**: The concept of making gaming accessible to everyone, regardless of physical capability, showcases the profound impact of inclusive design principles.

Through this project, I hope to explore the wider use of speech technology in entertainment and open up new possibilities for accessible game design.


## Research Question

The core question of this project is:

**"How can voice recognition technology be effectively applied to control the game Snake, enabling hands-free operation with response times and accuracy that meet the demands of real-time gameplay?"**

In addition, the project will investigate the feasibility and performance optimization strategies for using deep learning models on resource-constrained embedded systems to process voice commands.


## Application Overview

This project develops a voice-controlled Snake game that consists of several key components:

- **Voice Recognition Module:** This module collects audio through a microphone, capturing short commands such as "up," "down," "left," and "right," along with background noise and non-command sounds.
- **Data Preprocessing and Feature Extraction:** This involves processing the audio data to clip effective commands and extracting sound features using techniques like Mel Frequency Cepstral Coefficients (MFCC).
- **Deep Learning Model Training and Evaluation:** Utilizes various network architectures, such as 1D-CNN, on the Edge Impulse platform to train and evaluate models, aiming to improve recognition accuracy and response speed.
- **Command Execution Interface:** Deploys the trained model onto an embedded device (e.g., Arduino) and performs real-time recognition of user commands to control the direction of the Snake game.

The design focuses on model light-weighting and inference speed optimization to adapt to the computational capabilities of embedded devices while ensuring the smoothness and interactivity of the game experience.

**[Architecture Diagram: Project Structure]**  
![Architecture Diagram](URL_TO_DIAGRAM_IMAGE)



## Data

### Data Collection

The dataset for this project comprises six types of audio samples: command instructions ("up," "down," "left," "right"), "unknown" (random words), and "noise" (various background noises). Command samples were collected using smartphone microphones from 15 participants of diverse nationalities, genders, ages, and accents to enhance dataset diversity and improve the model's generalization capabilities. "Unknown" and "noise" samples were sourced from Edge Impulse's keyword spotting audio sample library (Edge Impulse, 2023a).

### Data Preprocessing

The preprocessing steps included:

1. **Sample Clipping:** Cutting out segments containing a keyword from longer audio files to ensure each clip contains only one clear command or noise.
   ![Sample Clipping](https://github.com/grandy0831/DL4SN-Voice-Controlled-Gluttonous-snake/assets/140076679/2c1f3581-3f2e-4ab9-afcc-e55bacbca24e)

2. **Audio Cleaning:** Manually removing audio clips with poor quality or recording errors.
   ![Audio Cleaning](https://github.com/grandy0831/DL4SN-Voice-Controlled-Gluttonous-snake/assets/140076679/66cb1939-6b8c-4593-b812-964fbef1c9e2)

3. **Duration Standardization:** All audio clips were processed to uniform length to maintain consistency during feature extraction.
4. **Label Annotation:** Each audio clip was accurately labelled to ensure precise correspondence between training data and labels.

### Dataset Construction

Approximately 300 samples per command were collected as raw data. Using the Edge Impulse platform, this data was automatically divided into an 80% training set and a 20% testing set. This division ratio helps the model learn sufficient features while retaining enough data to validate the model's generalization ability.
![Dataset Construction](https://github.com/grandy0831/DL4SN-Voice-Controlled-Gluttonous-snake/assets/140076679/4267c6ea-d3b3-4813-8818-55cffe2246ae)


### Feature Extraction

Mel Frequency Cepstral Coefficients (MFCC) techniques were employed to extract features from the audio. MFCC is extensively used in audio signal processing, particularly suitable for capturing qualitative characteristics of speech and music. It simulates the auditory perception of human ears, effectively capturing the short-term energy variations and spectral structure of audio signals, making it the preferred feature for sound recognition tasks(M. Rammo and N. Al-Hamdani, 2022).


## Model
This is a Deep Learning project! What model architecture did you use? Did you try different ones? Why did you choose the ones you did?

*Tip: probably ~200 words and a diagram is usually good to describe your model!*

## Experiments
What experiments did you run to test your project? What parameters did you change? How did you measure performance? Did you write any scripts to evaluate performance? Did you use any tools to evaluate performance? Do you have graphs of results? 

*Tip: probably ~300 words and graphs and tables are usually good to convey your results!*

## Results and Observations
Synthesis the main results and observations you made from building the project. Did it work perfectly? Why not? What worked and what didn't? Why? What would you do next if you had more time?  

*Tip: probably ~300 words and remember images and diagrams bring results to life!*

## Bibliography
*If you added any references then add them in here using this format:*

1. Last name, First initial. (Year published). Title. Edition. (Only include the edition if it is not the first edition) City published: Publisher, Page(s). http://google.com

2. Last name, First initial. (Year published). Title. Edition. (Only include the edition if it is not the first edition) City published: Publisher, Page(s). http://google.com

*Tip: we use [https://www.citethisforme.com](https://www.citethisforme.com) to make this task even easier.* 

----

## Declaration of Authorship

I, AUTHORS NAME HERE, confirm that the work presented in this assessment is my own. Where information has been derived from other sources, I confirm that this has been indicated in the work.


*Digitally Sign by typing your name here*

ASSESSMENT DATE

Word count: 
