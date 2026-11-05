# RAG Eval: Question Answering over RBI Documents

A retrieval-augmented question-answering system over public RBI circulars and master directions, built from scratch and evaluated on a hand-labelled question set.

## Goal

Answer questions about RBI regulations with cited sources (document and page), and measure how well each retrieval method finds the right page using recall@k and MRR.

## Status

Work in progress. Currently: project setup.

## Planned pipeline

1. Extract and clean text from PDFs, then split it into chunks
2. Retrieve with BM25, embeddings, and a hybrid of both
3. Rerank with a cross-encoder
4. Generate cited answers with an LLM
5. Evaluate everything on a hand-written benchmark

## Tech

Python, PyMuPDF, sentence-transformers, rank_bm25, FastAPI