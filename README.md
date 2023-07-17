# Project Overview

**NOTE**: This project is created to demonstrate MLOps skills by using the machine learning project from Towards Data Science [*article*](https://towardsdatascience.com/make-your-own-rick-sanchez-bot-with-transformers-and-dialogpt-fine-tuning-f85e6d1f4e30) by [Rostyslav Neskorozhenyi](https://www.linkedin.com/in/slanj/).

## Objective

The primary goal of this project is to develop a conversational AI model that can generate text in the style of Rick Sanchez, a character from the television show "Rick and Morty". This will be achieved by fine-tuning a pre-trained model on dialogues of Rick Sanchez to capture his unique conversational style and tone.

## Dataset

The training dataset consists of a collection of lines spoken by Rick Sanchez in the "Rick and Morty" show. The data will undergo preprocessing to ensure it is in a suitable format for model training. Any non-dialogue parts, such as stage directions or character names, will be removed to ensure the model is only trained on actual dialogues.

## Methodology

The method chosen to tackle this problem involves Transfer Learning, leveraging the DialoGPT model from the Hugging Face Transformers library. This model has been pre-trained on a vast corpus of internet text and provides a strong base for our task. The pre-trained model will be fine-tuned on the Rick Sanchez dialogues.

# Tools and Technologies

Several tools and technologies are employed in this project:

- **Azure**: Our chosen cloud platform, Azure hosts the necessary infrastructure and resources for the project.
- **Terraform**: An Infrastructure as Code tool used to set up and manage Azure resources.
- **Docker**: Ensures the creation of containerized applications of the model service, enabling easy deployment and scaling.
- **DVC**: Handles version control of the dataset.
- **MLflow**: Tracks the model's metrics and parameters during training and testing phases.
- **Jenkins**: Automates the process of building, testing, and deploying the model (CI/CD).
- **Kubernetes**: Manages and orchestrates the Docker containers in a production environment.

# Evaluation

As a generative model, traditional accuracy metrics do not apply. The model will be evaluated using Perplexity score, which measures how well the model predicts the sample. In addition, a qualitative analysis will be conducted by having team members interact with the bot and assess if its responses align with the style and tone of Rick Sanchez.

# Deployment and Monitoring

Once the model has been trained and evaluated, it will be containerized using Docker and deployed on Azure using Kubernetes. The performance of the deployed model will be continuously monitored using Azure Monitor and Azure Log Analytics. Alerts will be set up for any significant deviations in model performance or application health.

# Iterative Development

ML development is an iterative process. As results from the evaluation and deployment stages come in, the team may need to make adjustments to the model, its parameters, or even the data preprocessing steps. Tools like DVC and MLflow facilitate easy tracking of changes and experiments, making it straightforward to manage versions and compare different experiments.

