# 🤖 Unsupervised Learning & Reinforcement Learning Practical

## Customer Segmentation Using K-Means and Introduction to Reinforcement Learning

This practical explores two important areas of Artificial Intelligence and Machine Learning:

1. **Unsupervised Learning** — using K-Means Clustering for customer segmentation.
2. **Reinforcement Learning** — understanding agents, actions, rewards, exploration, and exploitation through a simple delivery-route example.

The practical focuses not only on Python implementation but also on understanding how these AI techniques can support **business decision-making**.

---

## 🎯 Learning Objectives

By completing this practical, the following concepts are demonstrated:

* Customer segmentation using K-Means Clustering
* Grouping similar customers based on their behaviour
* Interpreting customer clusters from a business perspective
* Understanding the basic concept of Reinforcement Learning
* Identifying an Agent, Action, Environment, and Reward
* Understanding Exploration vs Exploitation
* Connecting AI/ML techniques with real-world business applications

---

# 📊 Part A — Customer Segmentation Using K-Means

## 💼 Business Problem

An online retailer wants to understand the different types of customers it has.

The retailer has two main pieces of information:

* **Monthly Spending**
* **App Visits**

K-Means Clustering is used to divide customers into **3 groups** based on these characteristics.

---

## 📁 Dataset

A small customer dataset is created directly inside the notebook.

It contains:

| Customer | Monthly Spending | App Visits |
| -------- | ---------------: | ---------: |
| A        |             9000 |         20 |
| B        |             8500 |         18 |
| C        |             1200 |          3 |
| D        |             1500 |          4 |
| E        |             5000 |         10 |
| F        |             5500 |         12 |
| G        |             8800 |         19 |
| H        |             1800 |          5 |

The dataset represents different levels of customer spending and application activity.

---

## 🧰 Technologies Used

The clustering section uses:

* **Python**
* **Pandas**
* **Matplotlib**
* **Scikit-learn**
* **KMeans**

Pandas is used to create and manage the dataset, K-Means is used for grouping customers, and Matplotlib is used to visualize the resulting clusters.

---

## 🔍 Features Used for Clustering

The model uses:

```text
Monthly_Spending
App_Visits
```

The customer name is used only as an identifier and is not used as a clustering feature.

---

## 🤖 K-Means Clustering

The practical creates **3 clusters**:

```python
KMeans(
    n_clusters=3,
    random_state=42,
    n_init=10
)
```

The model assigns each customer to one of the three groups.

### Important Note

Cluster numbers such as:

```text
Cluster 0
Cluster 1
Cluster 2
```

do **not** automatically mean good, average, or bad customers.

The clusters must first be examined based on:

* Spending
* App visits
* Customer behaviour

before giving them a business name.

---

## 📈 Customer Segmentation Visualization

A scatter plot is created using:

* **X-axis:** Monthly Spending
* **Y-axis:** App Visits
* **Colour/group:** Cluster

Each customer is labelled on the graph to make the segmentation easier to understand.

### Example Business Segments

Depending on the clustering results, groups can be interpreted as:

* 💎 Premium Customers
* 📊 Medium-Value Customers
* 📱 Low-Engagement Customers

Possible business actions include:

* Loyalty rewards
* Personalized recommendations
* Re-engagement campaigns

---

# 🚚 Part B — Introduction to Reinforcement Learning

## 💡 What is Reinforcement Learning?

Reinforcement Learning is different from clustering.

The basic idea is:

```text
Take an Action
      ↓
Receive a Reward
      ↓
Learn from the Result
      ↓
Improve Future Decisions
```

The practical explains this concept through a simple delivery-route example.

---

## 🚛 Business Scenario

A delivery company has two possible routes:

* **Route A**
* **Route B**

The objective is to choose the route that generally results in faster delivery.

For simplicity:

* Fast delivery → Higher reward
* Slow delivery → Lower reward

---

## 🎁 Route Rewards

The practical defines the following example rewards:

```python
route_rewards = {
    "Route A": [5, 4, 6, 5, 4],
    "Route B": [8, 9, 7, 10, 8]
}
```

The average reward for each route is calculated to understand which route has historically performed better.

---

## 🧩 Reinforcement Learning Components

The delivery example demonstrates the main components of Reinforcement Learning:

| Component       | Example                                |
| --------------- | -------------------------------------- |
| **Agent**       | Delivery decision system               |
| **Environment** | Roads and traffic                      |
| **Action**      | Choose Route A or Route B              |
| **Reward**      | Feedback based on delivery performance |

The agent learns from the rewards received after taking actions.

---

# 🔎 Exploration vs Exploitation

An important Reinforcement Learning concept is the balance between **exploration** and **exploitation**.

### 🔍 Exploration

Exploration means trying a new or less-used option.

Example:

> Try Route A even when Route B has previously performed better.

The practical demonstrates exploration by randomly selecting one of the two routes.

### 🎯 Exploitation

Exploitation means selecting the option that is already known to perform well.

Example:

> Choose Route B because it has historically produced higher rewards.

The notebook demonstrates this by comparing the average rewards of Route A and Route B.

---

# 🆚 Machine Learning Comparison

The practical connects three major machine learning approaches with business applications:

| Machine Learning Type      | Main Idea                      | Business Example          |
| -------------------------- | ------------------------------ | ------------------------- |
| **Supervised Learning**    | Learn from known answers       | Customer churn prediction |
| **Unsupervised Learning**  | Discover hidden patterns       | Customer segmentation     |
| **Reinforcement Learning** | Learn from actions and rewards | Route optimization        |

---

# 💼 Business Applications

## Customer Segmentation

K-Means can help businesses:

* Identify different customer groups
* Understand customer behaviour
* Design targeted marketing campaigns
* Create personalized recommendations
* Provide loyalty benefits to valuable customers
* Re-engage less-active customers

## Reinforcement Learning

The route example demonstrates how reinforcement learning concepts can be applied to:

* Delivery route selection
* Transportation optimization
* Decision-making systems
* Dynamic resource allocation
* Reward-based business decisions

---

# 🛠️ Installation

Install the required Python libraries:

```bash
pip install pandas matplotlib scikit-learn
```

Then open the notebook using:

```bash
jupyter notebook
```

or upload it to **Google Colab**.

---

# ▶️ How to Run

### Google Colab

1. Open the `.ipynb` file in Google Colab.
2. Run the notebook from the beginning.
3. Execute each code cell.
4. Observe the K-Means customer clusters.
5. View the customer segmentation graph.
6. Calculate the average rewards for Route A and Route B.
7. Compare exploration and exploitation.
8. Complete the reflection questions.

The notebook is specifically structured as a Google Colab practical.

---

# 📂 Repository Structure

```text
Unsupervised-Reinforcement-Learning/
│
├── Unsupervised_and_Reinforcement_Learning_Practical_Name.ipynb
├── customer-segmentation.png
└── README.md
```

The practical's submission instructions specify renaming the notebook using the student's name, placing it under:

```text
part-a/unsupervised-learning/
```

and adding a screenshot of the customer-segmentation graph.

---

# 🧠 Key Concepts Learned

### Unsupervised Learning

* Clustering
* K-Means
* Customer segmentation
* Feature selection
* Cluster interpretation
* Business applications of segmentation

### Reinforcement Learning

* Agent
* Environment
* Action
* Reward
* Exploration
* Exploitation
* Reward-based decision-making

---

# 📌 Key Takeaways

### K-Means

K-Means helps businesses discover groups of customers with similar characteristics without requiring predefined labels.

### Reinforcement Learning

Reinforcement Learning allows a system to learn from the results of its actions by using rewards as feedback.

### Business Value

Both techniques can support better business decisions:

```text
Customer Data
     ↓
AI / ML Analysis
     ↓
Discover Patterns
     ↓
Understand Behaviour
     ↓
Make Better Business Decisions
```

---

# 🎓 Practical Outcome

This project provides a practical introduction to how different AI/ML approaches can solve different business problems.

The customer segmentation section focuses on **discovering hidden customer groups**, while the reinforcement learning section focuses on **learning from actions and rewards**.

---

# 📝 Reflection Topics

The practical also includes reflection questions covering:

1. What is Unsupervised Learning?
2. What is clustering?
3. What does K mean in K-Means?
4. How can customer segmentation help a business?
5. What is Reinforcement Learning?
6. What is an Agent?
7. What is an Action?
8. What is a Reward?
9. What is the difference between Exploration and Exploitation?
10. Which part of the practical was most useful for understanding business applications of AI?

---

# 👨‍💻 Project Information

**Project:** Unsupervised Learning & Reinforcement Learning Practical
**Primary Language:** Python
**Platform:** Google Colab / Jupyter Notebook
**Clustering Algorithm:** K-Means
**Dataset:** Small customer segmentation dataset
**RL Example:** Delivery route optimization
**Focus:** AI/ML concepts and business applications

---

## ⭐ Conclusion

This practical demonstrates two important approaches to machine learning.

**K-Means Clustering** is used to identify customer groups based on spending and app activity, while **Reinforcement Learning** is introduced through a delivery-route decision problem.

Together, these examples show how AI can help businesses understand customers, identify patterns, and make better decisions based on data and feedback.
# Unsupervised
Unsupervised &amp; Reinforcement Learning Practical | Customer segmentation using K-Means Clustering and an introduction to Reinforcement Learning through a business-focused route optimization example.  
