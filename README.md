# Meeting-Assistant-Agent

Speech-to-Text • Summarization • Q&A

An AI meeting assistant that transcribes meetings/lectures, summarizes discussions, and answers questions using a fine-tuned Whisper ASR model and a Gemma LLM, powered by Pinecone hybrid search (semantic + lexical retrieval) for accurate and grounded responses over long-form meeting content.

This system is designed for long-form meeting audio, supporting accurate transcription, semantic understanding, and interactive querying over meeting content.

✨ Features

🎙 Automatic Speech Recognition (ASR)

Fine-tuned Whisper model using QLoRA

Achieved ~9% Word Error Rate (WER) on evaluation set

📝 Meeting Summarization

Abstractive summaries using Gemma

Highlights key decisions, action items, and discussion points

❓ Meeting Q&A

Ask natural language questions about meeting content

Context-aware answers grounded in transcript

⚡ Efficient Training & Inference

QLoRA for low-memory fine-tuning

🧩 Hybrid Retrieval (Semantic + Syntactic Search)

Uses Pinecone Hybrid Search combining dense embeddings and sparse (lexical) vectors for more improved retrieval

# System Architecture 

    Audio Input
       ↓
    Whisper (Fine-tuned with QLoRA)
       ↓
    Meeting Transcript
       ↓
    Chunking
       ↓
    Dense Embeddings + Sparse Keywords
       ↓
    Pinecone Vector Store
       ↓
    Gemma LLM
       ├─ Abstractive Summarization
       └─ Retrieval-Augmented Q&A
   


QLoRa Adapters Link: https://huggingface.co/ibraheemaloran/whisper_qlora

