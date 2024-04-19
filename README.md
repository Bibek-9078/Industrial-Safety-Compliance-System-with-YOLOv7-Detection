# Industrial-Safety-Compliance-System-with-YOLOv7-Detection

**Problem Statement:**
Develop an automated system using the YOLOv7 detection model to ensure compliance with safety regulations in industrial settings. The system must:
- Accurately detect persons, vests, and helmet colors (blue, red, white, yellow) in real-time video frames.
- Classify individuals into various roles (electrician, fire department personnel, supervisor, worker) based on detected helmet and vest colors.
- Determine compliance status by matching helmet and vest colors to predefined roles.
- Identify instances of non-compliance when a person wears a helmet without a corresponding vest, correctly labeling their role and compliance status.

The solution aims to enhance safety protocols and streamline compliance monitoring processes in industrial environments.

# Dataset
- A novel dataset is constructed for detecting the helmet, the helmet colors and the person for this project.
- The dataset is open for free use, please download at

# Installation and Run
```
pip install -r requirements.txt  # install
python helmet.py --weights besthelmet.pt --conf 0.40 --img-size 640 --source source_path   #inference
```

# Download object detection model

Download object detection model manually:https://1drv.ms/f/s!AiUFkBjoGcsogtBu98SCnHrf07edVw?e=Sn2mjO



# STEPS:

1. **First detect the person ,vest and Helmet color(blue','red','white', 'yellow') in the frame using yolov7 detection model.**
   
   **Blue**: Electrician, **Red**: Fire department, **White**: Supervisor, **Yellow**: Worker

![3](https://github.com/Bibek-9078/Industrial-Safety-Compliance-System-with-YOLOv7-Detection/blob/main/image/3.jpg)

2. **Classify the Person on the basis of helmet color and vest weather the person is compliant or non-compliant**:

   ![1](https://github.com/Bibek-9078/Industrial-Safety-Compliance-System-with-YOLOv7-Detection/blob/main/image/1.jpg)

- if the person is wearing blue helmet and vest then it is consider as **Compiliant_Electrician**.

- if the person is wearing red helmet and vest then it is consider as **Compiliant_Fire-Department**.
  
- if the person is wearing white helmet and vest then it is consider as **Compliant_Supervisor**.
  
- if the person is wearing yellow helmet and vest then it is consider as **Compiliant_Worker**.
        

3. **Classify the Person on the basis of helmet color  and vest weather the person is compliant or non-compliant**.
   
   ![10](https://github.com/Bibek-9078/Industrial-Safety-Compliance-System-with-YOLOv7-Detection/blob/main/image/10.jpg)

- if the person is wearing blue helmet and not vest then it is consider as **non-Compiliant_Electrician**.
   
- if the person is wearing red helmet and not vest then it is consider as **non-Compiliant_Fire-Department**.

- if the person is wearing white helmet and not vest then it is consider as **non-Compliant_Supervisor**.

- if the person is wearing yellow helmet and not vest then it is consider as **non-Compiliant_Worker**.


# conclusion

The YOLOv7 detection model serves as a robust tool for ensuring compliance with safety regulations in industrial settings. By accurately detecting persons, vests, and helmet colors in real-time video frames, the model enables the classification of individuals based on helmet color and vest presence. Compliance criteria are clearly defined, allowing for the identification of compliant electricians, fire department personnel, supervisors, and workers based on their attire. Additionally, the model efficiently flags instances of non-compliance, such as when a person wears a helmet without a corresponding vest, thus aiding in maintaining safety standards within industrial environments.


