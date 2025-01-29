# LangChain: 
- open-source framework that allows developers to build applications using large language models (LLMs).
- LangChain's module-based approach allows developers to compare prompts and foundation models
- LangChain offers libraries in Python, JavaScript, and TypeScript.
- LangChain includes components that allow LLMs to access new data sets without retraining.
# GPT(Generative Pre-trained Transform):
- A type of artificial intelligence model developed by OpenAI that uses a Transformer-based neural network architecture.
- Generative: It can generate new text based on the input it receives.
- Pre-trained: Pre-trained on large datasets to learn language patterns, grammar, facts, and common sense knowledge.
- Transformer Architecture: GPT is based on the Transformer model, a deep learning architecture introduced in the paper "Attention Is All You Need" (2017).
  - Transformers rely on a mechanism called self-attention to analyze the relationships between words in a sequence, enabling them to understand context better than older models like RNNs(Recurrent Neural Network)) or LSTMs.
- Applications of GPT:
- Versions of GPT
  - GPT (Original): Introduced in 2018, with a small number of parameters.
  - GPT-2 (2019): A more advanced version with 1.5 billion parameters.
  - GPT-3 (2020): Significantly larger, with 175 billion parameters, enabling highly sophisticated responses.
  - GPT-4 (2023): Advanced multimodal capabilities, processing both text and images.
# RNN (Recurrent Neural Network):
- A type of neural network designed for sequential data.
- Unlike traditional feedforward networks, RNNs have loops that allow information to be passed from one step to the next, making them useful for tasks involving context or memory.
- Applications: Language modeling, Speech frecognition, Text generation
- Problems with RNNs:
  - Vanishing Gradient Problem: As the sequence length increases, the gradients (which help update weights during training) get smaller, making it difficult for the model to remember long-term dependencies.
  - Exploding Gradients: In some cases, the gradients become too large, causing unstable training.
# LSTM (Long Short-Term Memory):
  - A special type of RNN designed to handle the vanishing gradient problem by using a memory cell to store information over long sequences.
  - LSTMs can remember long-term dependencies, making them more effective in handling large sequences of data.
  - Instead of just one hidden state like an RNN, an LSTM has:
    - Cell State (Ct): Stores long-term memory.
    - Forget Gate: Decides what information to remove from the cell state.
    - Input Gate: Decides what new information to add.
    - Output Gate: Determines what information is sent to the next time step.
  - Applications: Machine translation, Sentiment Analysis, Time-series forecasting, Handwriting and speech recognition.
