# DeepLearning_FineTuneLLama2Project

Le but de ce projet est de d'utiliser une méthode QLORA avec un encodage 4bits pour entraîner un modèle de chat LLama2-7B afin de répondre à des questions d'étudiants de l'UQAC sur leurs programmes d'enseignement ou leurs cours.

Pour ce faire, des données ont été récupérés sur le site de l'UQAC avec des méthode de web scrapping. 
Ces données ont ensuites été utilisé pour entraîner le modèle suivant: https://huggingface.co/NousResearch/Llama-2-7b-chat-hf
Enfin, un pipeline a été constitués en ajoutant 
- un modèle d'embedding (https://huggingface.co/BAAI/bge-small-en-v1.5) en tant que modèle de RAG (retrieval agmented generation) afin d'aider le modèle à sélectionner les bonnes données pour répondre
- des techniques de prompt-engineering pour orienter la réponse du modèle

Les données utilisées sont trouvable dans le dossier "data", et les codes ayant permis de constituer ces différentes partie sont trouvables dans le dossier "src". 

Ces codes sources sont utilisables directement en les ouvrant dans google colab. C'est notament le fichier PipelineWithRAG permet de setup et d'utiliser le modèle que nous avons entraîné.


Remerciement à: 
- Krish Naik pour son tutoriel sur le fine tuning avec QLORA: https://colab.research.google.com/drive/1Bd7c5rioBOmtJbDEax83vAHEPru-r06l#scrollTo=OJXpOgBFuSrc
- et à Shaw Talebi pour son tutoriel sur la méthode RAG: https://colab.research.google.com/drive/1peJukr-9E1zCo1iAalbgDPJmNMydvQms?usp=sharing#scrollTo=WWiBVBuOUm-G
