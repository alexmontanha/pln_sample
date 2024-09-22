# Processamento de Linguagem Natural

O processamento de linguagem natural (PLN) é uma área da inteligência artificial que se concentra na interação entre computadores e linguagem humana. O objetivo do PLN é permitir que os computadores entendam, interpretem e gerem texto ou fala de maneira semelhante aos seres humanos.

Neste repositório, você encontrará recursos educacionais, atividades práticas e projetos relacionados ao processamento de linguagem natural. Os materiais são destinados a estudantes, educadores e entusiastas que desejam aprender mais sobre PLN e suas aplicações.

## Pré-requisitos

Para aproveitar ao máximo os recursos e atividades deste repositório, é recomendável ter conhecimentos básicos de programação em Python e familiaridade com conceitos de inteligência artificial e aprendizado de máquina.

Devem ser instaladas as seguintes bibliotecas Python:

- `nltk` (Natural Language Toolkit)
- `spacy` (Industrial-Strength Natural Language Processing)
- `textblob` (Simplified Text Processing)

´´´bash
pip install nltk
pip install spacy
pip install textblob
´´´

### Atividade Prática: Processamento de Linguagem Natural com Copilot ou ChatGPT

**Objetivo**: Reforçar o conceito e os métodos de processamento de linguagem natural (PLN) através de uma atividade prática utilizando Copilot ou ChatGPT.

**Descrição da Atividade**:
Os alunos irão desenvolver um projeto simples de PLN que envolve pré-processamento de texto, tokenização, análise de sentimento e reconhecimento de entidades nomeadas. Eles usarão Copilot ou ChatGPT para auxiliar na escrita do código e na compreensão dos conceitos.

**Passos da Atividade**:

1. **Introdução ao Projeto**:
   - Estude os conceitos de PLN que serão abordados: pré-processamento de texto, tokenização, análise de sentimento e reconhecimento de entidades nomeadas.

2. **Configuração do Ambiente**:
   - Configure um ambiente de desenvolvimento Python com as bibliotecas necessárias, como `nltk`, `spacy` e `textblob`.

3. **Pré-processamento de Texto**:
   - Utilize Copilot ou ChatGPT para escrever um código que realiza a limpeza e normalização do texto, removendo caracteres especiais, convertendo para minúsculas e removendo stop words.

   ```python
   import nltk
   from nltk.corpus import stopwords
   from nltk.tokenize import word_tokenize
   import string

   nltk.download('punkt')
   nltk.download('stopwords')

   def preprocess_text(text):
       # Converter para minúsculas
       text = text.lower()
       # Remover pontuação
       text = text.translate(str.maketrans('', '', string.punctuation))
       # Tokenizar palavras
       words = word_tokenize(text)
       # Remover stop words
       words = [word for word in words if word not in stopwords.words('english')]
       return words

   texto_exemplo = "Hello, world! This is a test sentence."
   palavras_processadas = preprocess_text(texto_exemplo)
   print(palavras_processadas)
   ```

4. **Tokenização**:
   - Utilize Copilot ou ChatGPT para escrever um código que realiza a tokenização de um texto em palavras.

   ```python
   from nltk.tokenize import word_tokenize

   texto_exemplo = "Hello, world! This is a test sentence."
   tokens = word_tokenize(texto_exemplo)
   print(tokens)
   ```

5. **Análise de Sentimento**:
   - Utilize Copilot ou ChatGPT para escrever um código que realiza a análise de sentimento de um texto utilizando a biblioteca `textblob`.

   ```python
   from textblob import TextBlob

   texto_exemplo = "I love programming. It's so much fun!"
   blob = TextBlob(texto_exemplo)
   sentimento = blob.sentiment
   print(sentimento)
   ```

6. **Reconhecimento de Entidades Nomeadas (NER)**:
   - Utilize Copilot ou ChatGPT para escrever um código que realiza o reconhecimento de entidades nomeadas utilizando a biblioteca `spacy`.

   ```python
   import spacy

   nlp = spacy.load("en_core_web_sm")
   texto_exemplo = "Apple is looking at buying U.K. startup for $1 billion"
   doc = nlp(texto_exemplo)

   for ent in doc.ents:
       print(ent.text, ent.label_)
   ```

7. **Discussão e Conclusão**:
   - Após a implementação, faça um resumo com os resultados obtidos e como cada método de PLN foi aplicado no projeto. Reforce a importância de cada etapa no processamento de linguagem natural.

**Recursos Adicionais**:
- Documentação das bibliotecas `nltk`, `spacy` e `textblob`.
- Exemplos de código e tutoriais online sobre PLN.

Essa atividade prática permitirá que os alunos compreendam melhor os conceitos de PLN e ganhem experiência prática utilizando ferramentas modernas como Copilot ou ChatGPT.