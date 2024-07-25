# Historic Artifact Restoration Advisor: RAG-Enhanced Chatbot

This project implements a Retrieval-Augmented Generation (RAG) chatbot specializing in historic artifact restoration advice. Using the Zephyr 7B Beta model and leveraging external knowledge, this chatbot provides expert guidance on artifact restoration and preservation.

## Features

- Expert advice on restoration techniques and preservation best practices
- Damage assessment guidance
- Historical context and significance explanations
- RAG-enhanced responses using a specialized knowledge base
- Customizable chat parameters (max tokens, temperature, top-p sampling)

## Technical Components

- **LLM Model**: Zephyr 7B Beta (via Hugging Face)
- **Embedding Model**: all-MiniLM-L6-v2 (Sentence Transformers)
- **Vector Database**: FAISS
- **UI Framework**: Gradio
- 
## Requirements

- Python 3.7+
- Dependencies listed in `requirements.txt`

## Installation

1. Clone this repository:
   ```
   git clone https://github.com/DavidMahey396/Customized-LLM-APP.git
   cd Customized-LLM-APP
   ```

2. Install dependencies:
   ```
   pip install -r requirements.txt
   ```

3. Run the application:
   ```
   python app.py
   ```

## Usage

After starting the application, interact with the chatbot through the Gradio interface. You can ask questions about artifact restoration, preservation techniques, or historical context. The chatbot will use RAG to provide informed responses based on your queries and its knowledge base.

Example queries:
- "How should I clean a 19th-century oil painting?"
- "What's the best way to preserve an ancient ceramic vase?"
- "Can you help me assess the damage on this antique wooden furniture?"

## Customization

You can adjust the chatbot's behavior using the additional inputs provided in the Gradio interface:
- System message: Define the chatbot's role and capabilities
- Max new tokens: Control the length of the generated responses
- Temperature: Adjust the randomness of the output
- Top-p (nucleus sampling): Fine-tune the diversity of the generated text

## How It Works

1. **Text Processing**: The app processes and stores text as documents.
2. **Vector Database**: Document embeddings are created and indexed for efficient retrieval.
3. **Query Processing**: User queries are embedded and compared against the document embeddings.
4. **RAG**: Relevant documents are retrieved and combined with the original query.
5. **Response Generation**: The LLM generates a response based on the augmented input.

## Contributing

Contributions to improve the chatbot are welcome. Please submit pull requests or open issues for any enhancements or bug fixes.

## Disclaimer

This chatbot is designed to provide general advice and information. For valuable or sensitive artifacts, always consult with a professional conservator or restoration expert.

## Contact

For any questions or concerns, please open an issue in this repository or contact da4368396@alphacollege.me

## Acknowledgements

- Hugging Face for providing the Zephyr 7B Beta model
- Sentence Transformers for the embedding model
- Gradio for the user interface framework
- FAISS for efficient similarity search
