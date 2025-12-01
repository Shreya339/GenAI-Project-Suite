# GenAI-Project-Suite
A suite of Generative AI projects, including Q&A chatbots, blog generators and multilingual document extractors using LangChain  to link powerful LLMs, such as OpenAI's GPT-3.5 and GPT-4, LLAMA2, Gemini Pro to an array of external data sources to create and reap the benefits of natural language processing (NLP) applications.

# Projects

## 1. Chat With PDF Using LangChain And Cassandra AstraDB
**[Repo Link](https://github.com/Shreya339/PDF-Query-with-OpenAI-and-CassandraDB)**

This project implements a **Retrieval-Augmented Generation (RAG)** pipeline using **Astra DB’s serverless Cassandra with Vector Search**, **LangChain**, and **OpenAI embeddings/LLMs**. A PDF is loaded in Colab, its text extracted and chunked, embedded using OpenAIEmbeddings, and stored in a Cassandra-backed vector store initialized via CassIO. User queries are embedded and matched against the stored vectors to retrieve the most relevant text segments, which are then fed to the OpenAI LLM to generate answers grounded in the retrieved content. The workflow includes PDF parsing, vector store creation, semantic similarity search, and an iterative Q&A loop managed through LangChain’s `VectorStoreIndexWrapper`.

---

## 2. Blog Generation Using LLAMA 2 LLM Models
**[Repo Link](https://github.com/Shreya339/LLAMA2-Blog-Generator)**

This project is a **local blog generation application** built using **Llama 2 (GGML)**, **LangChain**, and **Streamlit**. It loads a quantized Llama-2 7B Chat model directly from the local machine using **CTransformers**, enabling fast, fully offline text generation without any external APIs.  

The application allows users to generate blogs by providing a **topic**, **word limit**, and **writing style** (e.g., Researchers, Data Scientists, Common People). A custom LangChain `PromptTemplate` structures the inputs, and the model produces high-quality blog content optimized for clarity and coherence. The lightweight GGML **Q5_1 quantization** ensures efficient CPU-only inference, making it suitable even for low-resource environments.

---

## 3. Multi-Lingual Text Extractor
**[Repo Link](https://github.com/Shreya339/Gemini-Pro-MultiLingual-Document-Extractor)**

This project implements a **multimodal text-extraction and image-question-answering system** using **Google Gemini 1.5 Flash** integrated within a **Streamlit** interface. The pipeline accepts user-uploaded images (JPEG/PNG), performs byte-level preprocessing, and feeds both the raw image data and user queries into the Gemini Vision model via the `generate_content` API. The model performs **OCR-like multilingual text extraction**, followed by **context-grounded reasoning** to answer arbitrary questions about the image content.

---

## 4. Conversational Q&A Chatbot Using Gemini Pro API
**[Repo Link](https://github.com/Shreya339/QnA-Chatbot-GeminiAI)**

This project implements a **streaming chat application** using **Google Gemini Pro** and **Streamlit**. It maintains a persistent **chat history** in the session state and streams responses from the Gemini Pro model in real time. User inputs are sent to the model via the `start_chat` interface, and each chunk of the streamed response is displayed incrementally while updating the chat history. The system enables interactive, **multi-turn conversations** with the LLM, handling input, streaming output, and state management entirely within a lightweight web interface.
