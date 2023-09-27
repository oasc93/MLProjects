# Say Hello, to you new Biology study partner!

For 7 years I have tutored college students and tried to implement tools to help them understand the subject better. With the rise of large language models, I can deploy chatbots that are custom-trained on their course material to which they can ask questions they may have about the class.

This project is a custom-trained chatbot that can answer Biology questions.
It works by taking any PDF file that is place in the 'data' folder and creating the embeddings for the text. This will serve as the custom database that the model will use to answer your questions. The textbook used was 'Biology' by Openstax. Once the embeddings are made, we need a place to save the vector stores. This is done under the 'vector_store' folder using FAIIS. All of this takes place in the 'ingest.py' file. 

Now that ingestion has been completed, it is time to move on to the model and deployment. This project is designed to run entirely on CPU. The LLM used for this project is Meta's Llama 2. Chainlit was used to create the UI.

To deploy this project you will run model.py with the following command:
```bash
chainlit run model.py -w
```
