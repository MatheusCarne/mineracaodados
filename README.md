# Projeto de Mineração de Dados

## 🧑‍💻 Autores  
- Matheus Carneiro (202111250033) - matheus.cunha@academico.ifpb.edu.br  
- Thiago Matheus (202111250047) - thiago.honorato@academico.ifpb.edu.br   

## 🎯 Tema e Motivação  
O projeto aborda a recomendação de filmes com base nas avaliações feitas pelos usuários, buscando indicar os títulos mais prováveis de agradar cada pessoa. Diferente de simplesmente prever uma nota exata, o foco é identificar e ranquear os filmes mais recomendados para cada usuário, permitindo uma experiência personalizada. Sistemas desse tipo são amplamente usados por plataformas como Netflix, Amazon e Spotify, que se apoiam no histórico e no comportamento dos usuários para sugerir conteúdos relevantes.



## 📊 Conjunto de Dados Selecionado  
- **Nome do conjunto de dados:**  
    MovieLens 32M Dataset

- **Fonte:**  
  🔗 [GroupLens Research - MovieLens 32M](https://grouplens.org/datasets/movielens/32m/)

- **Descrição**  
Conjunto de dados público com **32 milhões de avaliações de filmes**, usado em sistemas de recomendação. Mantido pelo *GroupLens Research* (Universidade de Minnesota).  

- **Justificativa para a escolha:**  
  - **Grande escala e relevância estatística:**  
     - Permite análises robustas de preferências de usuários e padrões de avaliação.  
     - Ideal para testar algoritmos de recomendação (*collaborative filtering*, modelos híbridos).  

  - **Benchmark consolidado:**  
     - Amplamente utilizado em pesquisas acadêmicas e indústria, facilitando comparações com outros estudos.

---

## ❓ Perguntas ou Hipóteses  
-  **Problema principal:**  
   - Sugerir os filmes que cada usuário provavelmente vai gostar, mesmo que nunca tenha avaliado.
-  **Desafios:**  
    - Dados esparsos (muitos filmes com poucas avaliações).  
    - Precisão nas previsões para novos usuários/filmes.  

-  **Hipóteses:**  
    - Usuários dão notas parecidas para filmes do mesmo gênero.
    - Filmes populares têm avaliações mais consistentes.  

## 🔍 Metodologia  
-  Análise Exploratória de Dados (EDA) 
   - Entendimento das distribuições de notas, popularidade dos filmes e comportamento dos usuários.
-  Modelo de Filtragem Colaborativa com SVD  
    - O SVD (Singular Value Decomposition) foi usado para decompor a matriz de avaliações em fatores latentes, captando padrões escondidos sobre gostos de usuários e características dos filmes.  
    - A partir desses fatores, foi possível prever a probabilidade de um usuário gostar de filmes não avaliados.  
-  Refinamento com Regressão  
    - Utilizamos regressão para ajustar e refinar as previsões, buscando melhorar a ordenação dos filmes recomendados.
-  Geração da Lista de Recomendações 
    - Para cada usuário, listamos os filmes com maior previsão de interesse.

## 🛠️ Ferramentas Utilizadas  
- Python 🐍 — Linguagem de programação usada para todo o desenvolvimento.
- Pandas 📊 — Para manipulação e análise de dados em estruturas tabulares.
- NumPy 🔢 — Biblioteca para operações numéricas eficientes e manipulação de arrays.
- Scikit-learn 🤖 — Para modelagem preditiva, incluindo regressão logística, SVD, métricas e pré-processamento.
- SciPy — Biblioteca usada para operações avançadas, como similaridade com sparse matrices.
- Matplotlib e Seaborn 📈 — Para visualização gráfica dos dados e resultados.
- Random — Para seleção aleatória em amostras ou usuários.

## 📈 Resultados  
- O modelo conseguiu identificar com boa precisão os filmes mais prováveis de agradar cada usuário.
- As métricas indicaram que o sistema se comporta bem com usuários que possuem histórico consistente de avaliações.

## 📌 Conclusões  
O projeto permitiu implementar e comparar três abordagens distintas para sistemas de recomendação — **SVD**, **Regressão Logística** e **Rede Neural Profunda** — aplicadas ao dataset **MovieLens 32M**. Cada técnica apresentou pontos fortes e limitações, reforçando que não existe um “modelo único” ideal, mas sim soluções que variam conforme os objetivos e restrições do problema.

O **SVD** se destacou por gerar recomendações coerentes e populares, capturando padrões latentes entre usuários e filmes com boa precisão. A **Regressão Logística** teve desempenho técnico satisfatório, mas apresentou viés para títulos menos conhecidos, o que pode reduzir a aceitação das sugestões. Já a **Rede Neural**, utilizando embeddings e informações de gêneros, demonstrou flexibilidade para integrar múltiplas fontes de dados e capacidade de capturar relações mais complexas, oferecendo previsões mais personalizadas.

Durante o desenvolvimento, ficou evidente que **a qualidade e o pré-processamento dos dados são determinantes para o sucesso do sistema**. O dataset escolhido, apesar de robusto e amplamente utilizado em pesquisas, apresentou limitações como esparsidade elevada e concentração de avaliações em filmes antigos, o que impactou a diversidade e relevância das recomendações.

Entre os principais aprendizados, destacam-se:
- A importância de testar diferentes algoritmos e comparar seus resultados de forma quantitativa e qualitativa.  
- O fato de que modelos mais sofisticados nem sempre oferecem a melhor experiência prática para o usuário.  
- A necessidade de equilibrar **precisão técnica** e **usabilidade real** nas recomendações.  

Por fim, o projeto cumpriu seu objetivo de explorar técnicas de mineração de dados aplicadas à recomendação personalizada, fornecendo um panorama claro das vantagens e limitações de diferentes abordagens e abrindo espaço para melhorias futuras, como uso de datasets mais atuais, ajuste fino de hiperparâmetros e inclusão de novas variáveis contextuais.

## ⚠️ Limitações e Trabalhos Futuros  
- O dataset, apesar de grande, apresenta muitos dados esparsos.
- Para iniciar do zero, consideraríamos outro conjunto de dados mais balanceado em número de avaliações por filme.

---

