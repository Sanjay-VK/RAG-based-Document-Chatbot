# RAG-based-Document-Chatbot
An interactive Streamlit-based chatbot that analyzes resumes and answers user queries using NLP and vector similarity search. Built with Python, LangChain, FAISS, and deployed via Hugging Face and Ngrok. 
This project is an AI-powered chatbot that allows users to upload documents (PDF or DOCX) and ask questions based on their content. After uploading, the document is processed by extracting and cleaning the text. The text is then divided into smaller sections (chunks) for better understanding.

Each chunk is converted into a numeric representation (embedding) using a language model. These are stored in a FAISS vector database, which helps find the most relevant sections when a user asks a question. The chatbot then identifies the closest matching chunks and generates a response using the original document content.

The web interface is built with Streamlit, and the app can be accessed online via Hugging Face Spaces, Streamlit Cloud, or using Ngrok for local hosting. This tool helps users quickly extract accurate information from large documents through a simple Q&A interface.

Environment Setup
To start the project, make sure Python is installed on your system. Then, ensure all the necessary libraries are added. These include tools for:
- Building a web-based interface
- Reading document formats (PDF, Word)
- Processing natural language
- Generating text embeddings
- Enabling vector-based search for finding relevant content

These tools work together to help the chatbot understand and respond based on the uploaded document.
Uploading and Processing the Document
The chatbot allows users to upload a document through the web interface. Supported formats include PDF and Word (DOCX). Depending on the file type:
- PDF files are read page by page, and text is extracted.
- Word documents are read paragraph by paragraph.

After extraction, the text is cleaned by removing unnecessary characters and formatting, making it ready for further processing.
Splitting Text and Creating Embeddings
The cleaned document text is broken into smaller chunks (e.g., paragraphs or groups of sentences). This step makes it easier to analyze and retrieve information.

Each chunk is then converted into a numerical format (embedding) that captures the meaning of the text. These embeddings allow the system to compare text segments efficiently.
Storing and Searching Using a Vector Database
The embeddings are stored in a special type of storage known as a vector database. This database allows quick searches to find the most relevant chunks of the document when a user asks a question.

The question from the user is also converted into an embedding, which is then compared with the stored document chunks to find matches.
Answer Generation Based on Document
The chatbot fetches the chunks most related to the user's question. These chunks are used either directly or with the help of a language model to generate a clear and relevant answer. The answer is then shown in the chatbot window for the user.
Creating the Chat Interface Using Streamlit
Streamlit is used to build the user interface of the chatbot. It allows users to:
- Upload a document
- Type in their questions
- View the generated answers instantly

Streamlit automatically runs the application and shows everything in a simple, browser-based interface. This makes it easy for both developers and users to interact with the chatbot.
Hosting the Chatbot Using Ngrok
By default, the Streamlit application runs locally on the developer’s computer. To make it accessible from anywhere, a tool called Ngrok is used.

Ngrok creates a secure tunnel from a public link to the local chatbot server. When Ngrok is started, it gives a temporary web link. Anyone with this link can access the chatbot from their own devices, even though it's running locally on someone else's machine.

![image](https://github.com/user-attachments/assets/972cfc25-2491-4f91-a8f7-fe1d16786d06)

![image](https://github.com/user-attachments/assets/2da60ee4-b4cf-47d5-aa3e-f64dc2bb2438)

![image](https://github.com/user-attachments/assets/ea71d247-5deb-4666-88c3-0a537746834e)

![image](https://github.com/user-attachments/assets/812908c9-5851-4cb3-a252-73225f0ffc11)


![Uploading image.png…]()

Full Workflow Overview
1. User opens the chatbot web interface.
2. Document is uploaded (PDF/DOCX).
3. Text is extracted and cleaned.
4. Text is split into chunks and embeddings are created.
5. User types a question.
6. Question is compared with document embeddings.
7. Relevant parts are used to generate an answer.
8. Answer is shown in the web interface.
9. Using Ngrok, a shareable link is generated to let others access the chatbot online.
