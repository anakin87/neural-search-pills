# Open-source Neural Search/LLM frameworks

Today, you can easily access a wide variety of free NLP models or simply call paid API services based on Large Language Models.
But when it comes to building 🏗️ real-world NLP applications, the situation is more complex.

⚠️ you need these models to operate on your data/documents

⚠️ you need to store texts and embeddings in some kind of database

⚠️ you have to think from production perspective: building APIs, creating independent and scalable microservices...

**In many cases, using a Neural Search/LLM framework can simplify your life as a developer.**

## Notable frameworks

In 2021, I became interested in Neural and Semantic Search 🔎 and began to observe this ecosystem with curiosity, including the most popular frameworks. Then, at the end of 2022, we all observed a shift toward Large Language Models: some existing frameworks adapted, and others were born 👶.

I will try to list the most important open-source Neural Search/LLM frameworks that can help you develop your application quickly and robustly.

- [Haystack](https://github.com/deepset-ai/haystack) (by deepset) is a solid, well-structured, and documented NLP framework. It is also used by several major companies. Initially, it focused on making it easy to build end-to-end NLP-powered search systems based on your data. At the end of 2022, it introduced support for LLMs and, as of the most recent versions, allows you to develop LLM-based Agents 🕵️!

- [Jina](https://github.com/jina-ai/jina) (by Jina AI) is an MLOps framework for building multimodal 🖼️ AI applications. It provides a smooth experience in the transition from local applications to deploying and scaling microservices in Docker Compose/Kubernetes environments.

- [txtai](https://github.com/neuml/txtai) (by NeuML and David Mezzetti) is a simple open-source platform aimed at semantic search, supporting various workflows powered by language models 🔡. David also develops other interesting NLP libraries, such as txtchat and txtinstruct. These tools are capable of training and using small NLP models that can be run at low cost on low-resource environments, with good performance on a single task.

- [LangChain](https://github.com/hwchase17/langchain) 🦜️🔗 (by Harrison Chase) is probably the most popular Large Language Models framework. Launched in October 2022, it is still in an early and rapid phase of development, but it has already captured a lot of attention. It currently allows connecting a LLM to other sources of data and building Agents.

- [LlamaIndex](https://github.com/jerryjliu/llama_index) 🦙 (by Jerry Liu) is a recent project that provides an interface between LLMs and your data. In particular, it presents an extensive list of data connectors and also some interesting data structures for storing and retrieving information via Large Language Models.

- A special mention goes to the [Cheshire-Cat](https://github.com/pieroit/cheshire-cat) 😺 (by Piero Savastano 🇮🇹), a framework for developing intelligent Agents on top of several LLMs. It handles different types of memory and also provides a simple graphical interface.