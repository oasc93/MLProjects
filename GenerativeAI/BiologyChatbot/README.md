# Welcome to Your Biology Study Companion!

Are you ready to dive into the world of biology with a personalized study partner? Look no further! With over seven years of experience tutoring college students, I've developed a special tool just for you.

## About This Project

This project introduces a custom-trained chatbot, built to tackle your biology questions. 

### Step 1: Building the Knowledge Base

It starts by taking any PDF file in the 'data' folder and creating embeddings for the text within the PDF. Think of these embeddings as building blocks of knowledge. For this project, I've utilized the 'Biology' textbook by Openstax as our reference. The magic all happens in the 'ingest.py' file. If you would like to use your own data, you can insert any PDF into the data folder and run the 'ingest.py' file and it can become a chatbot for any information you'd like!

### Step 2: Storing the Knowledge

Once the embeddings are generated, we need a safe place to store these valuable building blocks. That's where the 'vector_store' folder comes into play, managed efficiently using FAIIS. This folder houses the foundation of our chatbot's knowledge. It currently contains the embeddings for the biology textbook referenced above.

### Step 3: Model and Deployment

This project is designed to run seamlessly on your CPU, ensuring accessibility for everyone. I employed Meta's Llama 2, a powerful Large Language Model (LLM), to bring this chatbot to life. Chainlit was used to craft the user-friendly interface.

## Getting Started

To deploy this project and have your biology questions answered, simply follow these steps:

1. Open your terminal or command prompt.
2. Run the following command:

   ```bash
   chainlit run model.py -w
   ```

And your biology study companion is ready to assist you.

## Accessing the Llama 2 Model

If you're interested in the Llama 2 model trained on a 7 billion parameters, you can access it through two repository:

- Hugging Face Repository: [Request Access](https://huggingface.co/meta-llama/Llama-2-7b)

Let's embark on this exciting biology journey together!
