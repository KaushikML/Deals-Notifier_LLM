
# **Deals-Notifier_LLM**

## 🚀 **Project Overview**
**Deals-Notifier_LLM** is an AI-driven system designed to scrape, analyze, and notify users of the best Amazon deals in real-time. By leveraging web scraping, a Chroma database, fine-tuned language models (LLMs), and modular agents, the system ensures timely notifications about valuable deals.

---

## 📂 **Repository Structure**
```
Deals-Notifier_LLM/
├── agents/
│   ├── deals.py                  # Defines the ScrapedDeal class and related functions
│   ├── ensemble_agent.py         # Estimates deal prices using AI models
│   ├── frontier_agent.py         # RAG-based deal pricer
│   ├── llama.py                  # LLaMA model integration
│   ├── messaging_agent.py        # Sends notifications via Pushover
│   ├── planning_agent.py         # Coordinates agent activities
│   ├── pricer_service.py         # Service for pricing deals
│   ├── scanner_agent.py          # Scrapes deals from RSS feeds
│   └── testing.py                # Contains test cases for agents
├── Database_Creation.ipynb       # Creates the Chroma database
├── Database_Visual_3D.ipynb      # Visualizes the database in 3D
├── Ensemble_Creation.ipynb       # Builds and trains the ensemble model
├── Final_Run.ipynb               # Executes the full pipeline
├── Model_Upload.ipynb            # Deploys fine-tuned models
├── Similar_Finder.ipynb          # Finds similar products using sentence-transformers
├── deal_agent_framework.py       # Framework for deal agents
├── price_is_right.py             # Main script to run the entire system
├── price_is_right_final.py       # Final version of the main script
├── pricer_ephemeral.py           # Ephemeral pricing service
├── pricer_service2.py            # Alternative pricing service implementation
├── .gitignore                    # Git ignore rules
├── environment.yml               # Conda environment configuration
├── LICENSE                       # License information
├── README.md                     # Project documentation
└── requirements.txt              # Required Python packages
```

---

## 🛠️ **Key Features**
- **Real-Time Scraping**: Utilizes `scanner_agent.py` to fetch deals from RSS feeds.
- **AI-Powered Price Estimation**: Employs an ensemble of fine-tuned LLMs and machine learning models in `ensemble_agent.py`.
- **Notification System**: Sends real-time deal alerts via Pushover using `messaging_agent.py`.
- **Modular Agent Framework**: Coordinates various agents through `planning_agent.py` for efficient workflow management.

---

## 💻 **Getting Started**

### **Prerequisites**
- **Python 3.9** or higher.
- Required Python libraries (detailed in `requirements.txt`).

### **Setup Instructions**
1. **Clone the Repository**
   ```bash
   git clone https://github.com/KaushikML/Deals-Notifier_LLM.git
   cd Deals-Notifier_LLM
   ```

2. **Set Up the Environment**
   - **Using Conda**:
     ```bash
     conda env create -f environment.yml
     conda activate deals-notifier
     ```
   - **Using Virtual Environment**:
     ```bash
     python3 -m venv env
     source env/bin/activate  # On Windows, use `env\Scriptsctivate`
     pip install -r requirements.txt
     ```

3. **Configure API Keys**
   - Create a `.env` file in the root directory with the following content:
     ```
     OPENAI_API_KEY=your_openai_api_key
     DEEPSEEK_API_KEY=your_deepseek_api_key
     HUGGINGFACE_API_KEY=your_huggingface_api_key
     PUSHOVER_USER=your_pushover_user_key
     PUSHOVER_TOKEN=your_pushover_api_token
     ```

---

## 🚀 **Execution Steps**

1. **Model Deployment**
   - **Notebook**: `Model_Upload.ipynb`
   - **Purpose**: Deploy fine-tuned models, including GPT-4o Mini, LLaMA 3.1, and the Random Forest Regressor.

2. **Database Creation**
   - **Notebook**: `Database_Creation.ipynb`
   - **Purpose**: Create the Chroma database with over 400,000 product data points.

3. **Ensemble Model Creation**
   - **Notebook**: `Ensemble_Creation.ipynb`
   - **Purpose**: Set up and fine-tune the ensemble model, combining predictions from various AI models.

4. **Similar Product Finder**
   - **Notebook**: `Similar_Finder.ipynb`
   - **Purpose**: Implement the sentence-transformer model (`all-MiniLM-L6-v2`) to find similar products based on descriptions.

5. **Final Execution**
   - **Notebook**: `Final_Run.ipynb`
   - **Purpose**: Execute the complete pipeline, including:
     - Scraping deals.
     - Analyzing and estimating prices.
     - Sending notifications to users via Pushover.

---

## 🛠️ **Technology Stack**
- **Programming Languages**: Python
- **Machine Learning Frameworks**: Scikit-learn
- **Large Language Models**: GPT-4o Mini, LLaMA 3.1
- **Database**: Chroma for vector similarity search
- **Web Scraping**: BeautifulSoup
- **Deployment**: Modal
- **Notification System**: Pushover

---

## 🤝 **Contributing**
Contributions are welcome! Please follow these steps:
1. **Fork the Repository**
2. **Create a New Branch**
   ```bash
   git checkout -b feature-name
   ```
3. **Commit Your Changes**
   ```bash
   git commit -m 'Add a feature'
   ```
4. **Push to the Branch**
   ```bash
   git push origin feature-name
   ```
5. **Submit a Pull Request**

---

## 📝 **License**
This project is licensed under the **MIT License**. See the [LICENSE](LICENSE) file for details.

---

## 📬 **Contact**
For questions, suggestions, or collaboration opportunities, feel free to open an issue in this repository.

