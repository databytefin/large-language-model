- query ---tokenization--> token
- token -> token id (by vocabulary list)
- token id -> embedding vector
- embedding vector -> vector db

- doc ---chunking--> chunk (important)
-

- compare the consine similarity
  - top-k: show the most relevant top k items
  - relevance score: usually 0 to 1

- top-k items --reranker--> reranked top-k items
- reranked top-k items + query -> prompt
- prompt -> LLM

```
why can't feed 100-page doc into LLM?
- context window
- high token cost
- long response time
```

---

chunking:

- fixed-size chunking (character) + overlap
- chracter splitting
  - first \n\n
  - then .
  - then \n or space
- semantic chunking (話題轉就chunk)
- content-specific chunking (e.g. table, text, graph)

---

hybrid search

- keyword search (BM25)
- semantic search

---

vector db

chroma: lightweight
milvus: production

---

graph rag
