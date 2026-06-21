# Study Material: Introduction to AI & Machine Learning

Hello, AI Builder! 🚀  
Welcome to your first study packet. This guide will help you review what we learned in our first session and walk you through your first hands-on AI project.

---

## 📝 Lesson Recap: In a Nutshell

*   **Normal Computers** are like **recipe books**. They only do exactly what we write down in the rules. If a rule says "toast the bread," it toasts. If you put a toy inside instead of bread, it still tries to toast it because it doesn't have a rule telling it not to!
*   **Artificial Intelligence (AI)** is different. Instead of coding rules, we feed the computer lots of examples (called **Data**). The computer looks at these examples, finds the **Patterns** (like color, shape, or texture), and learns how to make decisions on its own.
*   **Machine Learning (ML)** is the method we use to train these AI brains.

---

## 🗂️ The AI Dictionary (Key Terms)

1.  **Artificial Intelligence (AI)**: A computer program designed to act, think, and make decisions like a smart human or animal.
2.  **Machine Learning (ML)**: A way of teaching computers where they learn from examples and experiences instead of being given direct instructions.
3.  **Data**: Information used to train AI. For images, "data" is the photos. For voice, "data" is the sound clips.
4.  **Training**: The process where a computer scans data to look for patterns.
5.  **Model**: The "digital brain" that is created after the computer finishes training. It can be used to make guesses or predictions.
6.  **Pattern**: Details that repeat. For example, all apples have a stem, are roughly round, and are usually red, green, or yellow.

---

## 🛠️ Home Activity: Build Your Own Smart Camera!

You are going to build a real AI model that can tell the difference between two things using your webcam.

### 📍 Setup Instructions:
1.  Open your web browser and go to: **[teachablemachine.withgoogle.com](https://teachablemachine.withgoogle.com/)**
2.  Click the blue button that says **Get Started**.
3.  Select **Image Project**, then click **Standard image model**.

---

### 📍 Step-by-Step Training Guide:

#### Step 1: Name Your Classes
*   You will see two boxes labeled **Class 1** and **Class 2**.
*   Rename them to what you want to recognize. Examples:
    *   `Pen` vs. `Pencil`
    *   `Smiling Face` vs. `Silly Face`
    *   `Glasses On` vs. `Glasses Off`

#### Step 2: Record Your Data
*   Click the **Webcam** button in the first class box.
*   Hold down the **Hold to Record** button.
*   **Tip**: Move the object around, tilt your head, or change your distance from the camera so the computer gets different angles. Aim for **50 to 100 images** for each class.
*   Repeat this for the second class with the other object or expression.

#### Step 3: Train Your Brain!
*   Click the **Train Model** button in the middle column.
*   **Do not close the tab** or minimize the window while it is training. It will take about 10-15 seconds.

#### Step 4: Test & Play
*   Look at the **Preview** panel on the right side of the screen.
*   Show one of the objects to the webcam. Watch the confidence bars (percentages) move. Does it guess correctly?
*   Try a completely new object (e.g., if you trained on a blue pen, show it a red pen). Does it still know it's a pen?

---

## 📓 My AI Reflection Sheet
*Write down your answers or discuss them with your mentor in our next class!*

1.  **What did you train your AI to recognize?**
    *   Class 1: ________________________
    *   Class 2: ________________________
2.  **How accurate was your model?**
    *   [ ] Perfect (Guessed 100% correctly every time)
    *   [ ] Pretty Good (Guessed right most of the time)
    *   [ ] Confused (Kept mixing up the two classes)
3.  **Try to "trick" your AI. What made it make a mistake?**
    *(For example: Did it mistake your hand for the pencil? Did it get confused when you turned off the lights?)*
    *   What happened: __________________________________________________
4.  **If you wanted to make your AI even smarter next time, what should you do?**
    *   [ ] Record more images with different backgrounds and lighting.
    *   [ ] Train it for a longer time.
    *   [ ] Use different objects that look less alike.
