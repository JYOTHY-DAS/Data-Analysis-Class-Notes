# Day3: Today's class was about the historical development of AI. The class was presented by Mr. Sajil CK
### First he introduced us to a machine developed by Germany in WW II for data encryption named as ENigma- II. Mr.Sajil said that modern computing started from the attempts to decrypt these messages. Mr. Allen Turing was key figure in braking these encrypted messages and now he is known as the father of modern computer.

### Then we discussed about the concept of neural networks. He said that the idea of neural networks originated from the concept of neural pathway development in humans. Neuroplasticity is the adapting ability of brain which we can use in training neural networks.

### In 1958 Frank Rosenblatt developed the Mark I Perceptron machine  which is based on Perceptron algorithm developed by Warren McCulloch and Walter Pitts. The algorithm imitated the way neurons in the brain process information, and that enabled a system to learn from examples. We can say that it is a single layer neural network algorithm.
(include S.jpg here)

### A neuron will produce an output only if it receives a sufficient number of input signals, collectively at the dendrites. But if the amount of input signal is insufficient, the neuron will not produce an output. Perceptron mimicked the same method. It sums up the weighted inputs and if the result is above  a threshold value, it produces an output.


### 'Perceptrons: An Introduction to Computational Geometry' is a book written by Marvin Minsky and Seymour Papert and published in 1969. The crux of this book is a number of mathematical proofs which acknowledge some of the perceptron's strengths while also showing major limitations. The book proved that Perceptron machine won't be able to learn XOR function. After the publication of this book researchers started to question  the ability of 'Perceptron' to learn. The question raised was, if it cannot learn basic functions like XOR how can it learn complex activities like walking, talking, writing etc.

(include p.png here)

###  The limitations of Perceptron led to a loss of confidence in the potential of neural networks. Governments and industries became less willing to invest in AI research. This period is called as AI winter(mid-1970s to the early 1980s).

###Geoffrey Everest Hinton(Godfather of AI): His contributions to the development of multiple neuron models have been instrumental in advancing the field of AI.
He started a free course in [Coursera](https://www.youtube.com/playlist?list=PLoRl3Ht4JOcdU872GhiYWf6jwrk_SNhz9) on neural networks and machine learning. He received Nobel prize for physics in 2024.

## GPUs: The Powerhouses of Neural Network Training
### Why GPUs for Neural Networks?

- ### Graphics Processing Units (GPUs), originally designed for rendering graphics, have become indispensable tools for training neural networks. This is due to their:

- ### Massive Parallel Processing Power: GPUs are designed to handle many tasks simultaneously, making them ideal for the matrix operations involved in neural network training.
- ### High Memory Bandwidth: GPUs have large amounts of high-bandwidth memory, allowing them to quickly access and process the large datasets required for training complex models.
- ### Specialized Hardware Accelerators: Modern GPUs often include specialized hardware accelerators, such as Tensor Cores, that are specifically designed to accelerate deep learning operations.
- Popular GPU Choices for Neural Network Training: 1)NVIDIA GeForce RTX Series 2) NVIDIA Tesla Series 3) AMD Radeon RX Series

### DARPA(Defense Advanced Research Projects Agency) grand challenge: Fully autonomous vehicles have been an international pursuit for many years. The DARPA Grand Challenge is a prize competition for American autonomous vehicles, funded by the DARPA, the most prominent research organization of the United States Department of Defense. The Grand Challenge was the first long distance competition for driverless cars in the world. In the first DARPA challenge(2004) none of the robot vehicles finished the route. 

### The second DARPA Grand Challenge, 2005 played a pivotal role in accelerating the development of autonomous vehicle technology and, consequently, the broader field of AI. Here's why it was so significant:   

- ### 1. Catalyzed Technological Innovation:

### Pushed the Boundaries: The challenging off-road course forced teams to develop innovative solutions for perception, navigation, and control systems.   
### Accelerated Research: The competition spurred intense research and development efforts, leading to significant advancements in sensor technologies, computer vision, and machine learning algorithms.   

- ### 2. Fostered Collaboration and Knowledge Sharing:   

### Diverse Teams: The event brought together researchers from academia, industry, and government, fostering collaboration and knowledge exchange.   
### Open-Source Culture: Many teams shared their code and data, accelerating the development of autonomous vehicle technology for the entire community.

- ### 3. Laid the Foundation for Future Advancements:

### Technological Building Blocks: The technologies developed for the Grand Challenge, such as LiDAR, radar, and computer vision algorithms, became foundational for self-driving cars and other autonomous systems.   
### Inspiring the Next Generation: The event inspired young engineers and scientists to pursue careers in robotics and AI, ensuring a pipeline of talent for future innovation.

- ### 4. Demonstrated the Potential of AI:

### Public Awareness: The Grand Challenge showcased the potential of AI to solve complex real-world problems.   
### Investor Interest: The success of the event attracted significant investment into autonomous vehicle technology, fueling further research and development.   
### In essence, the DARPA Grand Challenge 2005 served as a catalyst for the rapid advancement of autonomous vehicle technology and AI as a whole.

### It demonstrated the power of competition, collaboration, and technological innovation to drive significant breakthroughs.
## AGI(Artificial general intelligence)
Artificial General Intelligence (AGI) refers to the hypothetical intelligence of a machine that possesses the ability to understand or learn any intellectual task that a human being can. It's a type of artificial intelligence (AI) that aims to mimic the cognitive abilities of the human brain.   

Key characteristics of AGI:

Generalization ability: AGI can transfer knowledge and skills learned in one domain to another, enabling it to adapt to new and unseen situations effectively.   
Learning and adaptation: AGI can learn from new information and experiences, making it capable of continuous improvement and evolution.
Reasoning and problem-solving: AGI can think critically, analyze information, and solve complex problems.
Self-awareness and consciousness: While not a strict requirement, some definitions of AGI include the ability to have subjective experiences and self-awareness.
Current state of AGI:

While significant progress has been made in AI, true AGI remains a theoretical concept. Current AI systems are specialized in specific tasks, such as image recognition or natural language processing. Creating an AI that can perform any intellectual task at a human level is a complex and challenging goal.

## AI, Machine Learning, and Deep Learning: A Hierarchical Relationship
### Artificial Intelligence (AI)
#### Broadest definition: AI is the science of making intelligent machines, especially intelligent computer programs.   
#### Goal: To create intelligent agents that can reason, learn, and make decisions.   
### Machine Learning (ML)
####   Subset of AI: ML is a subset of AI that focuses on algorithms that allow computers to learn from data without being explicitly programmed.   
#### Goal: To develop algorithms that can learn patterns from data and make predictions or decisions.   
### Deep Learning (DL)
#### Subset of ML: DL is a subset of ML that uses artificial neural networks with multiple layers to learn complex patterns from large amounts of data.   
#### Goal: To mimic the structure and function of the human brain to solve complex problems.
### Data Science: Use application of both machine learning and deep learning to extract insights from data.
(insert Hierarchy.png)

## Correlation vs. Causation: A Key Distinction
### Correlation and causation are two concepts often confused, yet they have distinct meanings.   

### Correlation
### Definition: Correlation refers to a statistical measure that indicates a relationship between two variables. It quantifies the strength and direction of this relationship.   
### Key point: Correlation does NOT imply causation.   
### Example: Ice cream sales and drowning deaths are often positively correlated. However, eating ice cream doesn't cause drowning. A third variable, like warmer weather, influences both.   

### Causation
### Definition: Causation implies a cause-and-effect relationship between two variables. One variable directly influences the other.   
### Key point: Causation requires a deeper understanding of the underlying mechanisms and often involves controlled experiments.   
### Example: Smoking causes lung cancer. This is a causal relationship, supported by extensive scientific research.   

### Why is it important to distinguish between correlation and causation?

### Avoiding Misinterpretations: Incorrectly assuming causation can lead to flawed conclusions and poor decision-making.   
### Identifying True Relationships: Understanding the causal relationships between variables is crucial for effective problem-solving and scientific research.
### Making Informed Decisions: By recognizing the difference, we can make evidence-based decisions and avoid falling for false correlations.
### As the complexity of models and datasets increases, we often rely more on pattern recognition, it's important to remember that causal inference remains a valuable goal in many applications. ### The choice between pattern matching and causal inference depends on the specific problem, the available data, and the desired outcome.
   
## Major Branches of Machine Learning

(insert Branches.png)

### Machine Learning is a vast field with various branches, each with its own unique approach to learning from data. Here are the primary branches:

Supervised Learning
In supervised learning, algorithms are trained on a labeled dataset. This means that each data point is associated with a correct output. The goal is to learn a mapping function that can predict the output for new, unseen data.

Classification:
Categorizes data into discrete classes.
Examples: Email spam detection, image classification (cat vs. dog), disease diagnosis.
Regression:
Predicts a continuous numerical value.
Examples: Predicting house prices, stock prices, or temperature.
Unsupervised Learning
Unlike supervised learning, unsupervised learning deals with unlabeled data. The goal is to discover hidden patterns and structures within the data.   

Clustering:
Groups similar data points together.
Examples: Customer segmentation, document clustering, image segmentation.
Association Rule Mining:
Discovers relationships between items in a dataset.
Examples: Market basket analysis (e.g., people who buy bread also buy milk).
Reinforcement Learning
Reinforcement learning involves training an agent to make decisions in an environment to maximize a reward signal.

Examples: Game playing (e.g., AlphaGo), robotics, autonomous vehicles.




 



