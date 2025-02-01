
# **Amazon Deals Notifier with AI-Powered Agents**

## 🚀 **Project Overview**
The **Amazon Deals Notifier** is an AI-driven system designed to scrape, analyze, and notify users of the best Amazon deals in real-time. By leveraging web scraping, a Chroma database, fine-tuned models, and modular agents, the system ensures users receive timely notifications about valuable deals.

---

## 📂 **Repository Structure**
```
Deals-Notifier_LLM/
├── agents/
│   ├── scanner_agent.py          # Scrapes deals from RSS feeds
│   ├── ensemble_agent.py         # Estimates deal prices using AI models
│   ├── messaging_agent.py        # Sends notifications via Pushover
│   ├── planning_agent.py         # Coordinates agent activities
│   └── frontier_agent.py         # RAG-based deal pricer
├── Database_Creation.ipynb       # Creates the Chroma database
├── Database_Visual_3D.ipynb      # Visualizes the database in 3D
├── Ensemble_Creation.ipynb       # Builds and trains the ensemble model
├── Final_Run.ipynb               # Executes the full pipeline
├── Model_Upload.ipynb            # Deploys fine-tuned models
├── Similar_Finder.ipynb          # Finds similar products using sentence-transformers
├── deal_agent_framework.py       # Framework for deal agents
├── price_is_right.py             # Main script to run the entire system
└── README.md                     # Project documentation
```

---

## 💻 **How to Run the Project**

### **Prerequisites**
1. Install **Python 3.9** or higher.
2. Ensure the required Python libraries are installed (refer to imports in the code files).
3. **Create a `.env` file** in the root directory to store your API keys:
   ```
   OPENAI_API_KEY=your_openai_api_key
   DEEPSEEK_API_KEY=your_deepseek_api_key
   HUGGINGFACE_API_KEY=your_huggingface_api_key
   PUSHOVER_USER=your_pushover_user_key
   PUSHOVER_TOKEN=your_pushover_api_token
   ```

---

### **Execution Steps**
1. **Model Deployment**
   - **Notebook**: `Model_Upload.ipynb`
   - **Purpose**: Deploy fine-tuned models, including GPT-4o Mini, LLaMA 3.1, and the Random Forest Regressor.

2. **Database Creation**
   - **Notebook**: `Database_Creation.ipynb`
   - **Purpose**: Create the Chroma database with over 400,000 product data points.

3. **Ensemble Model Creation**
   - **Notebook**: `Ensemble_Creation.ipynb`
   - **Purpose**: Set up and fine-tune the ensemble model, combining predictions from GPT-4o Mini, LLaMA 3.1, and the Random Forest Regressor.

4. **Similar Product Finder**
   - **Notebook**: `Similar_Finder.ipynb`
   - **Purpose**: Implement the sentence-transformer model (`all-MiniLM-L6-v2`) to find similar products based on descriptions.

5. **Final Execution**
   - **Notebook**: `Final_Run.ipynb`
   - **Purpose**: Execute the complete pipeline, which includes:
     - Scraping deals.
     - Analyzing and estimating prices.
     - Sending notifications to users via Pushover.

---

## 🛠️ **Technology Stack**
- **Machine Learning**: GPT-4o Mini, fine-tuned LLaMA 3.1, Random Forest Regressor.
- **Database**: Chroma (vector database for similarity search).
- **Web Scraping**: `BeautifulSoup` and RSS feed parsing.
- **Deployment**: Modal (serverless platform with $30 free credit).
- **Notification System**: Pushover for mobile alerts.
- **UI**: Gradio for interactive deal exploration.

---

## 📱 **Agent Workflow**
1. **Scanner Agent**: Scrapes deals from RSS feeds.
2. **Ensemble Agent**: Estimates deal prices using AI models.
3. **Messaging Agent**: Sends mobile notifications via Pushover.
4. **Planning Agent**: Coordinates the activities of all agents.
5. **Frontier Agent**: Implements a Retrieval-Augmented Generation (RAG) approach for deal pricing.

---

## 📊 **System Functionality**
- **Interval**: Refreshes every 5 minutes.
- **Process**:
  1. Scrapes live deals.
  2. Analyzes deals using the ensemble model and Chroma database.
  3. Sends high-value deal notifications directly to users' mobile devices.

---

## 🤝 **Contributing**
1. **Fork the Repository**: Click on the 'Fork' button at the top right of this page.
2. **Create a New Branch**: Use the command `git checkout -b feature-name`.
3. **Commit Your Changes**: `git commit -m 'Add a feature'`.
4. **Push to the Branch**: `git push origin feature-name`.
5. **Submit a Pull Request**: Navigate to the 'Pull Requests' tab and click 'New Pull Request'.

---

## 📝 **License**
This project is licensed under the **MIT License**. For more details, see the [LICENSE](LICENSE) file.

---

## 📬 **Contact**
For questions, suggestions, or collaboration opportunities, feel free to connect via LinkedIn or raise an issue in this repository.

---
