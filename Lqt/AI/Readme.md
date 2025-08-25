#  AI assistant for PDF

An AI-powered system that reads and understands various kind of PDF documents, allowing users to ask questions (Contextually) and receive contextually accurate answers based on the document content

## Features

- **PDF Upload & Processing**: Supports multiple PDF file uploads
- **Intelligent Text Chunking**: Smart content segmentation by paragraphs and sentences
- **Vector Database Storage**: FAISS-based similarity search for efficient retrieval
- **AI-Powered Answers**: Uses OpenAI GPT for generating apt responses
- **Persistent Storage**: Processed data is saved locally for future sessions
- **Web Interface**: Clean Streamlit-based UI for easy interaction

## Tech Stack

### Backend
- **Python 3.8+**
- **Streamlit** - Web interface framework
- **PyPDF2** - PDF text extraction
- **FAISS** - Vector database for similarity search
- **Sentence Transformers** - Text embedding generation

### AI/NLP Libraries
- **OpenAI GPT-3.5-turbo** - Answer generation
- **all-MiniLM-L6-v2** - Sentence embedding model
- **NumPy** - Numerical computations

## Installation & Setup

1. **Clone the repository**
   ```bash
   git clone <repository-url>
   cd pdf-ai-assistant
   ```

2. **Create virtual environment**
   ```bash
   python -m venv venv
   source venv/bin/activate  # On Windows: venv\Scripts\activate
   ```

3. **Install dependencies**
   ```bash
   pip install -r Write_Text.txt
   ```

4. **Get OpenAI API Key**
   - Sign up at [OpenAI](https://platform.openai.com/)
   - Create an API key from the dashboard
   - Keep it ready for use in the application

## How to Run

1. **Start the application**
   ```bash
   streamlit run app.py
   ```

2. **Open in browser**
   - The app will automatically open at `http://localhost:8501`
   - If not, manually navigate to the URL shown in terminal

## How to Use

### Step 1: Configure API Key
- Enter your OpenAI API key in the sidebar
- This is required for generating AI responses

### Step 2: Upload PDFs
- Click "Choose PDF files" in the sidebar
- Select one or more PDF documents
- Click "Process PDFs" to analyze the documents

### Step 3: Ask Questions
- Once processing is complete, enter your question in the main interface
- Click "Search & Answer" to get AI-powered responses
- View the answer along with relevant source context

## System Architecture

```
User Upload PDF → Text Extraction → Intelligent Chunking → 
Embedding Generation → Vector Database Storage → 
Query Processing → Similarity Search → Context Retrieval → 
AI Answer Generation → Response Display
```

### Core Components

1. **PDFProcessor Class**
   - Handles PDF text extraction using PyPDF2
   - Implements intelligent text chunking algorithm
   - Generates embeddings using SentenceTransformer
   - Manages FAISS vector database operations

2. **LLMHandler Class**
   - Manages OpenAI API integration
   - Handles prompt engineering for context-aware responses
   - Processes AI-generated answers

3. **Streamlit Interface**
   - Provides user-friendly web interface
   - Handles file uploads and user interactions
   - Displays results with source context

## Data Storage

- **Vector Database**: `data/vector_db.index` (FAISS index)
- **Text Chunks**: `data/chunks.pkl` (Processed text segments)
- **Metadata**: `data/metadata.pkl` (Source file information)

All processed data persists between sessions, so you don't need to reprocess PDFs every time.

## Error Handling

The system includes comprehensive error handling for:
- Invalid PDF files
- API connection issues
- Missing configuration
- File system errors
- Empty or corrupted documents

## Limitations

- Requires OpenAI API key (paid service)
- Performance depends on PDF quality and text extractability
- Vector similarity search may not capture all semantic relationships
- Limited to text-based PDFs (no OCR for scanned documents)
- Memory usage scales with document size and quantity


## Sample Use-Cases for Diffrent types of PDF 

1. **Business Documents**: Uploads company reports, policies, or manuals
   - Query: "What are the key financial metrics mentioned?"
   
2. **Research Papers**: Uploads academic papers or studies
   - Query: "What methodology was used in this research?"
   
3. **Legal Documents**: Uploads contracts or agreements
   - Query: "What are the termination conditions?"

## Troubleshooting

### Common Issues

1. **"No module named 'faiss'"**
   - Solution: Ensure you installed `faiss-cpu` not `faiss`

2. **OpenAI API errors**
   - Check your API key is valid and has available credits
   - Ensure you're using the correct API key format

3. **PDF processing fails**
   - Verify the PDF contains extractable text (not scanned images)
   - Try with a different PDF to isolate the issue

4. **Slow performance**
   - Large PDFs take longer to process
   - Consider breaking large documents into smaller sections


## Future Enhancements

Potential improvements that could be added:
- Support for other file formats (Word, Excel, etc.)
- OCR capability for scanned documents
- Multiple language model support
- Advanced chunking strategies
- Export functionality for answers
- User authentication and data management
