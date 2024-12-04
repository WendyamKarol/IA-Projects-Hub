# PDF Query Bot

## Introduction
------------
**Query Bot** est une application Python qui vous permet d'interagir avec plusieurs documents PDF. Vous pouvez poser des questions sur le contenu des PDF en utilisant un langage naturel, et l'application vous fournira des réponses pertinentes basées sur le contenu des documents. Cette application utilise un modèle de langage pour générer des réponses précises à vos questions. Veuillez noter que l'application répond uniquement aux questions liées aux fichiers PDF chargés.


## Fonctionnement
------------

![Fonctionnement Schematique](./docs/PDF-LangChain.jpg)

L'application suit ces étapes pour fournir des réponses à vos questions :

1. **Chargement des PDF** : L'application lit plusieurs documents PDF et en extrait le contenu textuel.
2. **Découpage du texte** : Le texte extrait est divisé en morceaux plus petits, appelés "chunks", afin d'être traité de manière efficace.
3. **Modèle de Langage** : L'application utilise un modèle de langage pour générer des représentations vectorielles (embeddings) des morceaux de texte.
4. **Correspondance de similarité** : Lorsque vous posez une question, l'application la compare aux morceaux de texte et identifie les plus similaires sémantiquement.
5. **Génération de la réponse** : Les morceaux sélectionnés sont envoyés au modèle de langage, qui génère une réponse basée sur le contenu pertinent des PDF.

## Dépendances et Installation 
----------------------------
Pour utiliser Query Bot**, suivez les étapes ci-dessous :

1. Installez les dépendances requises en exécutant la commande suivante :
   ```bash
   pip install -r requirements.txt
   ```

2. Obtenez une clé API d'OpenAI et ajoutez-la dans le fichier .env du répertoire du projet :
```commandline
OPENAI_API_KEY=your_secrit_api_key
```

## Utilisation
-----
Pour utiliser QueryBot, suivre les étapes suivantes :
1. S'assurez-vous d'avoir installé les dépendances nécessaires et ajouté votre clé API OpenAI dans le fichier `.env`.
2.Exécutez le fichie `main.py` en utilisant le CLI de Streamlit. Exécutez la commande suivante :
   ```
   streamlit run app.py
   ```
3. L'application s'ouvrira dans votre navigateur par défaut et affichera l'interface utilisateur.

4. Chargez plusieurs documents PDF dans l'application en suivant les instructions fournies.
   
5. Posez des questions en langage naturel sur les PDF chargés à l'aide de l'interface de chat.



## Licence 
-------
Query Bot est sous licence MIT.[MIT License]
