
**Nome:** Bruno Francisco Rodrigues Mafra, **RA:** 11201811147

**Nome:** Beatriz Sofientini Ribeiro, **RA:** 11202020433

**Nome:** Felipe Fernandes Gomes da Silva Costa, **RA:** 11202020223


## **Tema: Método avançado de filtragem de metadados baseado em grafos para melhorar a busca por similaridade vetorial em aplicações RAG**

Otimizando a busca por similaridade vetorial com técnicas baseadas em grafos usando LangChain e Neo4j.

___
Embeddings de texto nos ajudam a encontrar documentos se baseando em similaridade semântica, entendendo seus significados e quão semelhantes eles são entre si. Porém, eles nem sempre são eficientes para filtrar informações específicas, como datas ou categorias. Por exemplo, se você precisa encontrar documentos de um ano específico ou de uma categoria específica como "Ficção Científica", os embeddings podem não dar conta sozinhos ou as vezes fornecem resultados não muito precisos, daí surge a necessidade de filtragem de metadados, permitindo restringir resultados com base em atríbutos específicos.

___
## **O que faremos?**
Usaremos o mesmo dataset do exemplo acima chamado "companies", disponível em um servidor de demonstração público hospedado pelo Neo4j e iremos implementar um agente da OpenAI com uma única ferramenta, que pode gerar dinamicamente instruções Cypher (linguagem de consulta do Neo4j) com base na entrada do usuário e recuperar artigos relevantes do banco de dados de grafos.

Neste exemplo, a ferramenta terá quatro parâmetros de entrada opcionais:

- **Tópico (topic)**: Qualquer informação ou tópico específico, além de organização, país e sentimento, no qual o usuário está interessado.

- **Empresa (organization)**: A organização sobre a qual o usuário deseja encontrar informações.

- **País (country)**: O país das organizações nas quais o usuário está interessado.

- **Sentimento (sentiment)**: O sentimento dos artigos.

Usaremos a resposta obtida pela consulta ao banco para recuperar informações relevantes do grafo e usá-las como contexto para gerar a resposta final utilizando um modelo de linguagem (LLM).
