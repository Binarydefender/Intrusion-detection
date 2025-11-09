# Intrusion Detection System

## What We Did

We built an AI model to automatically look at computer network logs and decide if the traffic was **'Normal'** or an **'Attack'**.

We used a famous dataset called **NSL-KDD** and built the model using **Python** and **Scikit-learn**.

## How We Did It (The Steps)

1.  **Load Data:** We loaded the main training file (`KDDTrain+.txt`).

2.  **Clean Data:** The data had text (like 'tcp', 'http'). The AI only understands numbers, so we converted all the text into numbers.

3.  **Balance Data:** The data had more 'Normal' traffic than 'Attack' traffic. We told the model to pay extra attention to the 'Attack' samples so it wouldn't get biased.

4.  **Train the AI:** We split our main file into a "training" set (70%) and a "testing" set (30%). We trained the AI on the first set and then tested it on the second.

## What We Found (The Results)

The model was extremely accurate at finding attacks it had been trained on.

**✅ Accuracy: 99.88%**

This means our model was almost perfect at finding attacks in our test data. It correctly identified nearly every 'Attack' and 'Normal' connection.


<img width="598" height="839" alt="image" src="https://github.com/user-attachments/assets/6373225f-0127-4a35-bdd3-5ab1228ab20a" />

---

## The "Extra Challenge" (What Happened with the *Other* File)

After we proved our model worked, we tested it on a *second, separate challenge file* (`KDDTest+.txt`).


**⚠️ Accuracy on this file: 77.9%**

### Why was it so low?

This file was a **trick**. It contains **new types of attacks** that the model had **never seen before** during training.

### What This Means (In Simple Terms)

1.  Our model is **excellent** at finding attacks it has been trained to look for.
2.  An AI model is **not magic**. If a brand new, never-before-seen attack appears, it will probably miss it (just like our model did).

<img width="591" height="823" alt="image" src="https://github.com/user-attachments/assets/408c6bff-ab52-41c9-9411-f663385cb200" />
