# Welcome to Your Biology Study Companion!

Are you ready to dive into the world of biology with a personalized study partner? Look no further! With over seven years of experience tutoring college students, I've developed a special tool just for you.

## About This Project

This project introduces a custom-trained chatbot, purpose-built to tackle your biology questions. How does it work, you ask? Let me break it down for you:

### Step 1: Building the Knowledge Base

We start by taking any PDF file you provide and placing it in the 'data' folder. Next, we create embeddings for the text within the PDF. Think of these embeddings as building blocks of knowledge. For this project, we've utilized the 'Biology' textbook by Openstax as our reference. The magic all happens in the 'ingest.py' file.

### Step 2: Storing the Knowledge

Once the embeddings are generated, we need a safe place to store these valuable building blocks. That's where the 'vector_store' folder comes into play, managed efficiently using FAIIS. This folder houses the foundation of our chatbot's knowledge.

### Step 3: Model and Deployment

Our project is designed to run seamlessly on your CPU, ensuring accessibility for everyone. We've employed Meta's Llama 2, a powerful Large Language Model (LLM), to bring this chatbot to life. Chainlit, our trusty companion, was used to craft the user-friendly interface.

## Getting Started

To deploy this project and have your biology questions answered, simply follow these steps:

1. Open your terminal or command prompt.
2. Run the following command:

   ```bash
   chainlit run model.py -w
   ```

And voilà! Your biology study companion is ready to assist you.

## Accessing the Llama 2 Model

If you're interested in the Llama 2 model trained on a whopping 7 billion parameters, you can access it through two repositories:

- Hugging Face Repository: [Request Access](https://huggingface.co/meta-llama/Llama-2-7b)
- Meta Repository: [Request Access](https://huggingface.co/meta-llama/Llama-2-7b)

Let's embark on this exciting biology journey together!