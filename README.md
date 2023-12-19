# RAGkoon

Chatbot de questions réponses sur une base de code avec Langchain.

Basé sur ce
[guide de LangChain](https://python.langchain.com/docs/use_cases/question_answering/code_understanding#open-source-llms)
sur les embeddings avec du code.

## Installation

On utilise poetry. Cloner le repo et dans un terminal :

```shell
poetry install
```

Peu importe le modèle utilisé pour la génération, une clé OpenAI est nécessaire
pour créer les embeddings. Régler la variable d'environnement `OPENAI_API_KEY`
dans `./.env`.

### Pré-requis

- pyenv
- python >= 3.11.2
- poetry >= 1.7.1

```sh
pyenv install 3.11.2
pyenv use 3.11.2
poetry env use $(which python)
```

## Préparation

Alimenter un repo d'exemple dans le répertoire `./repo`

Choisir un modèle à utiliser. Dans `main.py`, la variable `llm` peut être
définie avec le modèle choisi dans
[les modèles de chat LangChain](https://python.langchain.com/docs/integrations/chat/)

Deux exemples sont présents dans `main.py`, GPT-4 et CodeLlama en local avec
Ollama. Pour utiliser un modèle local, il est nécessaire de lancer le serveur
Ollama dans un autre terminal :

```shell
ollama serve
```

## Génération

Dans un terminal, activer l'environnement python et lancer `main.py` :

```shell
poetry shell
python main.py
```
