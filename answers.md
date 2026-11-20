
# Answers Transformes Questions

## Attention questions

The dimensions of Q, K and V for a single head attention head (ignoring the batch dimension):
- seq_len, d_k
- seq_len, d_q
- seq_len, d_v

The output of QK^T of shape (seq_len, seq_len) represents the token-to-token compatability scores, which then gets multiplied by V to produce (seq_len, d_v). 
The multiplication with V becomes intuitive, as it essentially represents a weighted average applied across tokens (i.e. tells each token how much attention to 
pay to the other tokens).

The QK^T is a single matrix multiplication that can be computed much faster than other alternatives (e.g. cosine similarity, or a NN that learns the similarity score). 

The lower dimensionality of Q, K, V allows h heads to run in parallel for roughly the same compute cost as a single head.

## LSTM/RNN comparison

In the original LSTM, there are multiple gates that determine how information gets processed (across repeating NN layers):
- forgetting gate
- new information gate
- output gate

It is similar in a way to Transformers, as it outputs information based on the preceeding hidden states (e.g. compressed information from all previous tokens), but it "pays attention" to only the preceeding hidden value only (rather than taking into consideration all the other inputs). So in terms of recurrance, you keep applying the layers of LSTM one after another to each of the inputs, with persisting information from one step to another. The limitation is that you have to squeeze all the information in a single vector, rather than allowing for every token to look at each other.

In LSTM, every token has to be sequentially processed, whereas in Transformers they can all be processed simultaneously in parallel.

Decoder only Transformers do introduce time/sequence information via positional embedding and masking.

## Dense layers (i.e. projections) in Multi-head Attention

Each attention head has its own set of projections (W_k, W_q, W_v), so that they can learn different patterns from the provided input. For example, one head can learn to track subject-verb relationships, while a different one tracks words with long-range links. This would be the case in a single multi-head attention block, but modern implementation have multiple layers of attention-blocks, each individual one with multiple heads that have their own set of projections. This is the how these modern systems learn complex patterns.

## Importance of skip connections

Without skip connections around attention functions:
- after multiple rounds of taking a weighted average ofß weighted averages all tokens will converge to the same vector (rank collapse)
- embedded positions would be lost
- gradients would vanish, making it impossible to train the network.

Skip connections in Transformers should be cosnidered a "highway of information", where each attention layer computes contextual update, updating the previous token identity.



