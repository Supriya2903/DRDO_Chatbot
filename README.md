# DRDO Chatbot

## Overview
This project is an intelligent chatbot built during my DRDO (Defence Research and Development Organisation) internship. The chatbot provides information about DRDO by scraping official DRDO website content and implementing a sophisticated question-answering system using vector similarity search and AI-powered responses.

## Features
- **Web Scraping**: Automatically scrapes content from the official DRDO website
- **Vector Search**: Uses FAISS (Facebook AI Similarity Search) for efficient similarity search
- **AI-Powered Responses**: Integrates with Mistral AI API for generating contextual answers
- **Chat History**: Maintains conversation history using MongoDB
- **Interactive UI**: Built with Streamlit for a user-friendly chat interface
- **Real-time Processing**: Provides instant responses to user queries about DRDO

## Tech Stack

### Backend
- **Python**: Core programming language
- **FAISS**: Vector similarity search for document retrieval
- **Sentence Transformers**: Text embedding generation (`all-MiniLM-L6-v2`)
- **Mistral AI API**: Large language model for response generation
- **MongoDB**: Database for storing chat history
- **PyMongo**: MongoDB driver for Python

### Web Scraping
- **Playwright**: Async web scraping framework
- **Asyncio**: Asynchronous programming for concurrent scraping

### Frontend
- **Streamlit**: Web application framework for the chat interface

### Data Processing
- **NumPy**: Numerical computing for vector operations
- **JSON**: Data storage and processing
- **Pandas**: Data manipulation (if applicable)

## Project Structure
```
DRDO_chatbot/
├── DRDO1/
│   ├── app.py                 # Streamlit web application
│   ├── chatbot_backend.py     # Core chatbot logic
│   ├── mistral_api.py         # Mistral AI API integration
│   ├── faiss_utils.py         # FAISS index operations
│   ├── mongo_utils.py         # MongoDB operations
│   ├── drdo_scraper.py        # Web scraping script
│   ├── drdo_data.json         # Raw scraped data
│   ├── drdo_cleaned.json      # Processed data
│   ├── drdo_metadata.json     # Document metadata
│   ├── drdo_faiss.index       # FAISS vector index
│   └── chatbot.ipynb          # Jupyter notebook for development
└── README.md
```

## Use Cases
1. **Information Retrieval**: Quick access to DRDO-related information
2. **Research Assistant**: Helps researchers find relevant DRDO content
3. **Public Information**: Provides accessible information about DRDO's work
4. **Educational Tool**: Assists students and professionals learning about DRDO
5. **Knowledge Base**: Serves as a comprehensive DRDO information repository

## Installation and Setup

1. **Clone the repository**:
   ```bash
   git clone https://github.com/Supriya2903/DRDO_Chatbot.git
   cd DRDO_Chatbot
   ```

2. **Install dependencies**:
   ```bash
   pip install streamlit sentence-transformers faiss-cpu pymongo playwright mistral-ai requests numpy
   ```

3. **Set up Playwright**:
   ```bash
   playwright install
   ```

4. **Configure API Keys**:
   - Update `MISTRAL_API_KEY` in `DRDO1/mistral_api.py`
   - Ensure MongoDB is running locally on port 27017

5. **Run the application**:
   ```bash
   streamlit run DRDO1/app.py
   ```

## How It Works

1. **Data Collection**: The scraper (`drdo_scraper.py`) crawls the DRDO website and extracts content
2. **Vector Indexing**: Content is converted to embeddings using Sentence Transformers and indexed with FAISS
3. **Query Processing**: User queries are converted to vectors and matched against the indexed content
4. **Response Generation**: Retrieved context is sent to Mistral AI for generating human-like responses
5. **Chat Interface**: Streamlit provides an interactive chat interface with history tracking

## Development Notes

- **Internship Project**: Developed during DRDO internship program
- **Research Focus**: Combines web scraping, NLP, and AI for information retrieval
- **Scalable Architecture**: Modular design allows for easy extension and modification
- **Performance**: FAISS ensures fast similarity search even with large datasets

## Screenshots

![Screenshot 2025-04-07 221436](https://github.com/user-attachments/assets/bd4b7027-e422-4265-8914-998e0ec1cc0f)

![image](https://github.com/user-attachments/assets/59ebb555-9c48-41c7-8d53-b9fc68552324)

## Future Enhancements

- Add user authentication and personalized chat history
- Implement real-time website monitoring for content updates
- Add support for multiple languages
- Integrate with more AI models for improved responses
- Add analytics dashboard for usage tracking

## Contributing

Feel free to fork this project and submit pull requests for improvements!

## License

This project was developed during a DRDO internship and is shared for educational purposes.
