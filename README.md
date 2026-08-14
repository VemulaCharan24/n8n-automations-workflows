# n8n-automations-workflows
# Order Status Processing & Warehouse Sync (n8n Workflow)

An automated workflow built in **n8n** that connects to a warehouse API, retrieves item data, and intelligently filters/processes orders based on their current status (e.g., checking if an order is `processing`).

---

## 🚀 What This Workflow Does
1. **Manual Trigger:** Initiates the workflow execution on demand.
2. **API Data Fetching:** Connects to the warehouse endpoint using secure header authentication (`x-assessment-id`) to fetch inventory and order data.
3. **Conditional Routing:** Evaluates incoming data properties (such as `orderStatus`) using expressions to separate or route items depending on their current state.

---

## 🛠️ Tech Stack & Tools
* **Workflow Automation:** [n8n](https://n8n.io/)
* **Data Format:** JSON
* **Integration:** REST APIs

---

## ⚙️ How to Import & Run

If you want to run or test this workflow in your own n8n instance:

1. **Download the JSON:** Export the workflow `.json` file from your n8n editor.
2. **Import into n8n:** 
   * Open your n8n dashboard.
   * Click on **Workflows** -> **Import from File** (or drag and drop the JSON file into your workflows list).
3. **Configure Credentials / Headers:** 
   * Update the HTTP Request node with your specific API endpoint URL.
   * Ensure your required headers (like your `x-assessment-id`) are correctly configured.
4. **Execute:** Click **Execute Workflow** to test the pipeline!

---

## 📂 Project Structure
```text
├── workflow.json         # The exported n8n workflow file
└── README.md             # Project documentation
