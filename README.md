# BGE-M3 Qdrant sample. Hybrid search & reranking 

This repository contains a Jupyter notebook that demonstrates how to build an advanced search system using BGE-M3 and Qdrant.

The key feature of this sample is the use of an all-in-one embedding model (BGE-M3) that generates three types of vectors in a single pass:
- **Dense vectors**: For semantic similarity (1024 dimensions)
- **Sparse vectors**: For lexical/keyword matching
- **ColBERT token vectors**: For fine-grained token-level matching

This multi-vector approach provides superior search quality by combining the strengths of different embedding types within a single model.

## Requirements

- Python 3.9+
- Docker (for running Qdrant)
- Jupyter Notebook

## How It Works

The system operates in the following steps:

1. **Data Loading**: Products are loaded from a CSV file
2. **Text Formatting**: Product information is formatted for embedding
3. **Embedding Generation**: BGE-M3 generates all three embedding types in one pass
4. **Vector Database Setup**: Qdrant collection is configured for hybrid search
5. **Data Indexing**: Product data and embeddings are stored in Qdrant
6. **Search**: Queries go through the same embedding process and retrieve results
