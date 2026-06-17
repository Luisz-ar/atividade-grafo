# Grafo de Bairros de Curitiba

Projeto acadêmico em C que modela os **75 bairros de Curitiba** como um **grafo não-direcionado**, utilizando uma **matriz de adjacência** para representar as conexões (vizinhanças) entre eles.

## Sobre o projeto

Cada bairro é um vértice do grafo, e cada conexão entre dois bairros vizinhos é uma aresta. A matriz de adjacência (75x75) armazena essas relações: `matriz[i][j] = 1` indica que os bairros `i` e `j` são vizinhos; `0` indica que não há conexão direta entre eles.

O programa oferece um menu interativo com seis operações sobre o grafo:

| Opção | Funcionalidade |
|---|---|
| 1 | Testar conexão direta entre dois bairros (por índice) |
| 2 | Mostrar o grafo completo, listando os vizinhos de cada bairro |
| 3 | Listar todas as conexões de um bairro específico (por nome) |
| 4 | Adicionar uma nova conexão entre dois bairros |
| 5 | Remover uma conexão existente entre dois bairros |
| 6 | Verificar se a matriz é simétrica |

## Estrutura do código

O código é dividido em funções, cada uma responsável por uma operação do menu:

- **`buscarBairro`** — função auxiliar que busca um bairro pelo nome digitado pelo usuário e retorna seu índice na matriz (ou `-1` se não encontrado).
- **`testarConexaoDireta`** — verifica se existe conexão direta entre dois bairros, informados por índice.
- **`mostrarGrafo`** — percorre toda a matriz e exibe, para cada bairro, a lista de seus vizinhos.
- **`todasConexoesDeBairro`** — usa `buscarBairro` para localizar um bairro pelo nome e lista todas as suas conexões.
- **`adicionarConexao`** — adiciona uma aresta entre dois bairros, atualizando a matriz nas duas posições simétricas (`matriz[i][j]` e `matriz[j][i]`), garantindo que o grafo continue não-direcionado.
- **`removerConexao`** — remove uma aresta entre dois bairros, seguindo a mesma lógica de simetria.
- **`verificarSimetria`** — percorre o triângulo superior da matriz comparando `matriz[i][j]` com `matriz[j][i]`, identificando qualquer inconsistência na simetria do grafo.

## Sobre o desenvolvimento

Este foi um projeto acadêmico desenvolvido em grupo, no qual cada integrante implementou uma ou mais funções de forma independente. Minha contribuição específica foi a implementação das funções **`adicionarConexao`** e **`removerConexao`**, responsáveis por manter a integridade e a simetria da matriz a cada alteração no grafo.

Além disso, junto com outro colega do grupo, fui responsável por **integrar todas as funções desenvolvidas separadamente pelos membros**, padronizando o estilo do código (formatação, mensagens de saída, nomenclatura) para que todas as partes funcionassem de forma coesa dentro de um único programa.

## Tecnologias

- **Linguagem:** C
- **Estrutura de dados:** Matriz de adjacência (grafo não-direcionado)
