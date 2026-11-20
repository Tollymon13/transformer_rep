Embeddings 
- initialises word embedding weights (num_embeddings, embedding_dim) to map the input tokens ids to vectors (n_embd). During training, the weights get updated, such that these vectors cluster together into similar concepts (e.g. dog close to cat).
- initialise position embeddings weights (contex_size, embedding dim) that gets added on top of the word embeddings, which sets an offset between vectors. During training, these weights get updated such that these offsets are learned, separating words into positions (without loosing the meaning of those words).

Hyperparameters
- n_embd = 764 (nothing special about it, other that being computationally friendly)
- n_cntx = 1024 (cotnext size of each sequence of tokens processed, nowadays this is in its millions)
- n_vocab = 50,257 (vocabulary uses 256 base bytes to transform words into 50k tokens)