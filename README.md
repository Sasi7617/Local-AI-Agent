# Local-AI-Agent
Local AI Agent – Pizza Review Assistant (RAG Based)

This project is a Local AI Agent built using Retrieval-Augmented Generation (RAG) that answers user questions related to pizza reviews. The system uses a local dataset of pizza customer reviews containing information such as review titles, ratings, dates, and detailed feedback from customers.

Instead of relying solely on the knowledge of a Large Language Model (LLM), the application retrieves relevant information from a vector database created from the pizza review dataset. When a user asks a question (for example: “Which pizza has the best crust?” or “Are there good vegan pizza options?”), the system searches the dataset for the most relevant reviews and provides accurate answers based on the retrieved data.

The workflow of the system is as follows:

The pizza review dataset is converted into embeddings.

These embeddings are stored in a vector database (ChromaDB).

When a user asks a question, the system retrieves the most relevant reviews using semantic similarity search.

The retrieved context is passed to the LLM through a prompt template.

The LLM generates a response grounded in the retrieved pizza reviews.

This approach helps reduce hallucinations and ensures that the AI responses are factually grounded in the provided pizza review data.

The dataset contains diverse customer feedback including topics such as:

Pizza crust quality

Service experience

Pricing

Vegan and gluten-free options

Specialty pizza styles (Detroit, Chicago deep dish, NY style)

Ingredient quality

Delivery experiences

Restaurant atmosphere

By combining LangChain, vector embeddings, ChromaDB, and an LLM, this project demonstrates how RAG can be used to build domain-specific AI assistants that answer questions based on private data.

This simple project showcases the practical implementation of GenAI concepts like embeddings, vector databases, semantic search, and Retrieval-Augmented Generation in a real-world use case.
