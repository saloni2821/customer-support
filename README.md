Customer Support Ticket Analysis And Prevention System(PROJECT)
This repository contains the implementation of a Customer Support Ticket Analysis and Prevention System. The project is designed to enhance the efficiency of customer support by leveraging sentiment analysis, automated responses generation and issue escalation handliing, integrated seamlessly using FastAPI and Zapier.

Importance of Customer Support Ticket Analysis:
In today's fast-paced world, customer satisfaction is pivotal for any organization. Analyzing customer support tickets helps identify recurring issues, gauge customer sentiment, and streamline response mechanisms. This not only enhances the customer experience but also reduces the workload on support teams, allowing them to focus on critical tasks.

Project Structure:
Initial Data Analysis
The project begins with an exploratory data analysis conducted on two datasets located in the analysis folder under the rough directory. This step was crucial to:

Understand the structure and quality of the data.
Identify patterns and trends that inform the subsequent machine learning models.
Sentiment Analysis
This module determines the sentiment of the user based on their ticket. By classifying tickets into positive, neutral, or negative sentiments, the system:

Prioritizes tickets requiring immediate attention.
Provides insights into the overall customer satisfaction levels.
Key steps:

Preprocessing ticket data.
Training and testing a sentiment classification model.
Outputting the sentiment score for each ticket

SOME RESULTS:
This is an image of how the data is spread for different issues using heatmap



![WhatsApp Image 2025-02-03 at 19 39 43_bc726145](https://github.com/user-attachments/assets/ffe68029-ad5d-4e5b-8493-7163ea54f158)

The table above presents the F1 scores for different sentiment categories across various approaches in Natural Language Processing (NLP). The approaches evaluated are:

Basic: A simple baseline model with no prompt optimization.
Prompt Engineering: Refining prompts to improve model responses.
Few-Shot: Providing a few examples to guide the model in understanding the task.
Chain-of-Thought (COT): Encouraging step-by-step reasoning to enhance accuracy.
![Screenshot 2025-02-03 193631](https://github.com/user-attachments/assets/928c28fb-ccfc-4bd5-b8f1-b6145c294fc2)

Issue Escalation
This module identifies tickets requiring escalation based on specific keywords and patterns. If an issue is marked for escalation:

The ticket is forwarded to a human agent for review.
Automated responses are bypassed to ensure personalized handling.
Key steps:

Keyword-based filtering and rule-based classification.
Forwarding flagged tickets for manual intervention.

Response Automation
This module generates automated responses for tickets using two distinct approaches:

Classical Machine Learning and Transformer-based Classification:
Products are classified based on ticket content.
Predefined templates generate responses tailored to the classified product category.
Some results
This is a cluster visualization
![cluster automated](https://github.com/user-attachments/assets/21820d6f-2daf-449d-9fb9-29b19701e6e1)

Automated response on a prompt
![auto res](https://github.com/user-attachments/assets/ce1f6675-103d-427f-bd55-defd37591f1f)

Pipeline Using Gemini and Vector Search:
Embeddings are created using the ticket content.
Vector search retrieves the most relevant response.
A personalized response is generated based on context and user history.


Integration with FastAPI and Zapier
The entire system is integrated using FastAPI to expose API endpoints for each module. These endpoints are connected through Zapier to:

Automate workflows and email responses.
Seamlessly handle escalations and response generation.

REQUIREMENTS:
1. JSON Key for Google Sheets
2. OpenAI API Key
3. Pinecone API
4. Dataset
5. FastAPI and Uvicorn

Conclusion:
This Customer Support Ticket Analysis and Prevention System is a comprehensive solution for modern customer support challenges. By combining sentiment analysis, issue escalation, and automated responses, the system optimizes ticket handling and ensures customer satisfaction. The seamless integration with FastAPI and Zapier makes it scalable and adaptable to diverse business needs.

