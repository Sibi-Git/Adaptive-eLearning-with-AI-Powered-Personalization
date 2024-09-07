📚 **LearnAI: Adaptive eLearning Platform** 
🤖
==============================================

Welcome to **LearnAI**, an AI-powered adaptive eLearning platform designed to provide personalized learning experiences! 🚀 This platform leverages cutting-edge neural networks to dynamically adjust content based on user performance. Whether you're a student or an educator, LearnAI optimizes learning paths using data-driven insights. 🎓

📑 **Table of Contents**
------------------------

-   [🌟 Features](#-features)
-   [🛠️ Tech Stack](#%EF%B8%8F-tech-stack)
-   [🚀 Getting Started](#-getting-started)
    -   [Prerequisites](#prerequisites)
    -   [Installation](#installation)
-   [🎯 Technical Workflow](#-technical-workflow)
-   [📊 Performance Tracking](#-performance-tracking)
-   [🧠 Future Enhancements](#-future-enhancements)
-   [📫 Contact](#-contact)

🌟 **Features**
---------------

-   🔄 **Real-Time AI Personalization**: Utilizes neural networks (ANNs, RNNs) to customize learning content based on learner behavior, with adjustments made after every quiz or interaction.
-   🧠 **Diagnostic Assessments**: Automated quizzes that evaluate a user's knowledge level and adjust content difficulty accordingly.
-   📊 **Learning Rate Calculation**: Adaptive learning paths are optimized using historical performance data, with learning rates dynamically updated for every user.
-   📝 **Content Generation via Web Scraping**: Automatically fetches relevant articles and video content (e.g., from YouTube) based on the current topic being studied.
-   🧩 **Modular & Scalable Design**: The system is easily extensible with new courses, modules, or additional AI models.

🛠️ **Tech Stack**
------------------

-   **Frontend**:

    -   HTML5, CSS3, JavaScript (for dashboards and user interaction)
    -   Django templates (for rendering dynamic content)
-   **Backend**:

    -   **Django**: A Python-based web framework for managing users, sessions, and course content.
    -   **REST API**: Exposes content and user data via Django's REST Framework (DRF), allowing easy integration with external services.
-   **Machine Learning**:

    -   **TensorFlow** & **Keras**: For building, training, and deploying neural networks (ANNs, RNNs).
    -   **Model Types**: LSTM (Long Short-Term Memory) models for handling time-series data related to learner progress and performance.
    -   **Training Data**: Self-collected data stored in `.csv` files, covering multiple learning topics.
-   **Database**:

    -   **SQLite3**: Used for managing user data, course content, quizzes, and performance metrics.
-   **External APIs**:

    -   **YouTube API**: Used for fetching relevant educational videos.
    -   **BeautifulSoup & Requests**: For web scraping and pulling relevant article content for personalized learning.

🚀 **Getting Started**
----------------------

### Prerequisites

-   Python 3.8+
-   TensorFlow 2.4.0+
-   Keras 2.4+
-   Django 3.2+
-   Django REST Framework

### Installation

1.  Clone the repository:

    ```bash
    git clone https://github.com/Sibi-Git/learnai-adaptive-elearning-platform.git
    ```

2.  Navigate to the project directory:

    ```bash
    cd learnai-adaptive-elearning-platform
    ```

3.  Install required Python packages:

    ```bash
    pip install -r requirements.txt
    ```

4.  Apply database migrations:

    ```bash
    python manage.py migrate
    ```

5.  Run the development server:

    ```bash
    python manage.py runserver
    ```

6.  Visit `http://localhost:8000` to explore the platform.

🎯 **Technical Workflow**
-------------------------

1.  **User Registration & Preferences**:

    -   Users sign up and choose their content preferences (e.g., videos, articles).
2.  **Diagnostics Phase**:

    -   The platform starts with diagnostic quizzes to assess the learner's baseline knowledge. The results are fed into the neural network model for personalization.
3.  **Neural Network Personalization**:

    -   **Model Architecture**: Uses ANN and RNN layers (specifically LSTM) to predict user performance and adjust learning paths. Training data is based on previous users' performance data stored in `NN_Models`.
    -   **Content Adaptation**: Dynamically serves quizzes, articles, and videos according to the user's learning rate and content interaction.
4.  **Content Generation**:

    -   **Video Content**: Uses the YouTube API to fetch relevant videos based on the user's current learning unit.
    -   **Article Content**: Uses web scraping tools like BeautifulSoup to pull related articles from pre-configured sources.
5.  **Feedback & Learning Rate Update**:

    -   Performance is continuously monitored, and the learning rate is adjusted based on real-time quiz performance and engagement. **Learning rates** are stored in `lr.csv`, and updates are applied after every user interaction.

📊 **Performance Tracking**
---------------------------

-   The platform stores user scores and dynamically adjusts difficulty. The **feedback.py** script helps determine the optimal learning path using predefined thresholds for each topic.
-   Users can view progress reports that show quiz results and overall topic mastery.

🧠 **Future Enhancements**
--------------------------

-   🌐 **Advanced Analytics**: Add detailed user progress analytics using data visualization libraries like Matplotlib.
-   📱 **Mobile Integration**: Develop a mobile app version to extend accessibility.
-   💡 **AI Model Improvement**: Incorporate more sophisticated neural network models for further enhancing content personalization.

📫 **Contact**
--------------

👨‍💻 Developed by Sibi Marappan\
📧 Email: msibi.mail@gmail.com\
💼 [LinkedIn](https://www.linkedin.com/in/sibi-marappan/)\
🖥️ [GitHub](https://github.com/Sibi-Git)
