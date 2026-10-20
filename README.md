# Predicting Diabetes: Learning How Data Balancing Saves Lives

Hello and welcome to my project! 👋 

When I started learning about data science, I wanted to work on a real-world problem that actually matters to human lives. That is why I chose to build a machine learning model that looks at health records to predict whether a person might have diabetes. 

Throughout this project, I didn't just write code—I wanted to understand the **"why"** behind every step, especially when dealing with messy, real-world data problems like unfair data.

---

### 🏥 What is this project about?
Using a well-known health dataset, my goal was to take different health clues—like a person's glucose levels, body mass index (BMI), age, and blood pressure—and teach a computer to spot the early warning signs of diabetes. 

### ⚠️ The Big Problem I Ran Into: Unbalanced Data
When I first looked at the dataset, I noticed something very important:
* There were **500 healthy patients** 
* But only **268 diabetic patients**

If you feed a computer a dataset where one group is much larger than the other, the computer gets lazy. It learns to just guess "healthy" every time and still look right on paper. But in healthcare, missing a sick patient is dangerous! 

### 🛠️ How I Solved It (The Approach)
To fix this imbalance, I used a popular data-cleaning technique called **SMOTE** (Synthetic Minority Over-sampling Training data). 
1. **Cleaning and Scaling:** I prepared the data so that different measurements (like high glucose numbers versus smaller age numbers) were placed on a fair playing field.
2. **Balancing the Data:** Instead of deleting healthy records or just copy-pasting sick records, SMOTE intelligently created realistic, balanced training examples so the computer had a fair chance to study both sides equally.
3. **Training Two Models:** I built two identical models for a head-to-head race:
   * Model A: Trained on the *original* imbalanced data.
   * Model B: Trained on the *SMOTE-balanced* data.

---

### 📊 What Did We Find? (The Results)
When we gave both models a secret "final exam" (a hidden test set of patients they had never seen before), the results were eye-opening:

* **The Original Model:** Because it was blinded by the healthy majority, it missed nearly **half** of the actual sick patients. 
* **The SMOTE Model:** By balancing the data, our new model successfully caught **about 7 out of 10** actual diabetes cases, drastically reducing how many sick patients slipped through the cracks!

The comparison charts and final ROC performance curves proved that fixing your data before training makes a massive, life-saving difference.

---

### 🧰 Tools and Technologies Used
* **Python** for writing the code
* **Jupyter Notebook** for organizing my step-by-step workflow
* **Pandas** for managing data tables
* **Scikit-Learn & Imbalanced-Learn** for building models and data balancing
* **Matplotlib** for drawing charts and visual graphs

---

### 🌱 Final Thoughts
This project taught me that data science isn't just about throwing code at a computer—it’s about understanding the human impact behind the numbers. Thank you for checking out my work! If you have any questions or feedback, feel free to reach out.
