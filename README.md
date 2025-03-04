# IGBPD: Industry Guidance Business Process Dataset  

## 📖 Introduction  
Recent advancements in process mining have highlighted the challenges in making workflows more **readable** and **interpretable**. Large language models (LLMs) offer great potential in this area, but existing datasets often **lack critical contextual information**, limiting their effectiveness in analyzing real-world workflows.  

To address these challenges, we introduce the **Industry Guidance Business Process Dataset (IGBPD)**, a structured dataset built from **205 multi-industry guidance documents**. IGBPD provides a **comprehensive representation of business workflows** across diverse domains, serving as a robust resource for **process mining research and LLM-based workflow analysis**.  

This dataset is validated through **expert-based human evaluations** and **automated assessments**, demonstrating its utility in tasks such as:  
- **Workflow validation**  
- **Error detection**  
- **Next-step prediction**  

IGBPD also supports multiple indexing methods, ensuring its **adaptability** and **generalizability** across various analytical needs.  

🚀 **The dataset is publicly available at here**  

🚀 IGBPD provides a benchmark dataset bridging the gap between unstructured business process text and structured logical workflows, enabling cutting-edge research in process mining and LLM-based analysis.
---

## 📂 Dataset Structure  

The dataset is organized into two main folders:  

### **1️⃣ GraphData (Workflow Graph Representation)**  
This folder contains the **dependency relationships and node transitions** of business workflows.  
- `NodeJump.csv` → Workflow data **without** the Subdomain layer  
- `NodeJumpWhole.csv` → Workflow data **with** the Subdomain layer  
- `neo4jData/` → Neo4j-compatible versions of the dataset  

🔹 **Use case:** These files help analyze **workflow dependencies**, **process transitions**, and support **Neo4j-based graph exploration**.  

---

### **2️⃣ TaksData (LLM Evaluation Tasks)**  
This folder contains multiple test sets designed to evaluate the ability of **LLMs** to analyze and understand workflows.  

#### **Task 1: Workflow Correctness Classification**  
- **IC = 1** → Fully correct workflows  
- **IC = 0 or 1** → Workflows containing errors  

🔹 **Goal:** Test whether LLMs can **distinguish between correct and incorrect workflows**.  

#### **Task 2: Domain & Workflow Classification**  
This task evaluates LLMs' ability to **identify the correct domain, subdomain, and workflow** after removing certain hierarchical layers.  
- **Three different test files** with different levels of information removed.  

🔹 **Goal:** Assess whether LLMs can correctly classify workflows under **varied levels of missing information**.  

#### **Task 3: Next-Step Prediction under Missing Information**  
- Contains **23 test files**.  
- **TestsetDescription.xlsx** provides details on **which information is missing** in each test file.  

🔹 **Goal:** Evaluate LLM robustness in **predicting the next step** despite missing contextual details.  

---

## 🔍 How to Use the Dataset  
1️⃣ **Graph Analysis** → Use `GraphData` to explore workflow dependencies and relationships using **Neo4j** or **process mining tools**.  
2️⃣ **LLM Testing** → Use `TaksData` to benchmark LLMs for **workflow validation**, **classification**, and **next-step prediction**.  
3️⃣ **Custom Research** → Adapt the dataset to your specific needs in **AI-driven process mining** and **workflow automation**.  

---

📧 Contact
For any questions or collaborations, please contact:
📩 [Xiaohan.Su@student.uts.edu.au]

---

## 📜 Citation  
If you use **IGBPD** in your research, please cite:  
```bibtex
@article{your_reference,
  title={IGBPD: A Business Process Dataset in Multi-Industry Guidance Documents},
  author={Xiaohan Su, Bin Liang, Yifei Dong, Zhidong Li, Fang Chen},
  journal={[KDD]},
  year={2025}
}


