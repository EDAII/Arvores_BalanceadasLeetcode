# Arvores_BalanceadasLeetcode
# EDA II Leetcode

## Leetcode  
**Número da Lista:** 3
**Conteúdo da Disciplina:** Arvores Balanceadas

---

## 👥 Alunos
| Matrícula   | Aluno                      |
|-------------|-----------------------------|
| 21/1061897  | Igor de Sousa Justino      |
| 20/2016364  | Guilherme Coelho Mendonça  |

---

## Sobre
O projeto consiste na resolução de questões do LeetCode que envolvem **arvores balanceadas**

---

## 🔹 Problema 1: 1382. Balance a Binary Search Tree
**Nível:** Médio  
**Implementação:** Código 1  

Dado a root (raiz) de uma árvore binária de busca (BST), balanceie a árvore para garantir que a diferença de altura entre as subárvores de cada nó nunca seja maior que 1 e retorne a raiz da árvore balanceada.

Os passos do algoritmo para balancear a árvore são:

Fazer uma travessia in-order: Percorra a árvore e crie uma lista com os valores dos nós em ordem crescente.

Construir a árvore balanceada: A partir da lista ordenada, construa uma nova árvore binária de busca. A cada passo, o valor do meio da lista é escolhido como a raiz, garantindo que a árvore seja balanceada.

Repetir o processo: Continue criando as subárvores à esquerda e à direita recursivamente até que todos os nós estejam na nova árvore balanceada.

Algoritmo implementado:

Função inorder(node): Realiza uma travessia in-order e retorna os valores dos nós em ordem crescente.

Função sortedArrayToBST(nums): Cria uma árvore balanceada a partir da lista ordenada, escolhendo o valor do meio para ser a raiz.

Função balanceBST(root): Usa as funções anteriores para balancear a árvore e retornar a nova raiz balanceada.

Complexidade:

Tempo: O tempo é O(n), onde n é o número de nós, devido à travessia da árvore e à reconstrução da árvore balanceada.

Espaço: O espaço é O(n), devido à lista auxiliar e à pilha de chamadas recursivas.


<p align="center">
  <img src="assets\1382.png" alt="Print da Questão 1382" width="600"/>
</p>    

---

## 🔹 Problema 2:  102. Binary Tree Level Order Traversal
**Nível:** Médio  
**Implementação:** Código 2  

O problema exige a implementação da **traversal por nível** de uma árvore binária, ou seja, percorrer os nós da árvore da esquerda para a direita, nível por nível. Esse processo é uma aplicação da **busca em largura (BFS)**, onde a árvore é tratada como um grafo acíclico, já que uma árvore é um tipo específico de grafo.

O algoritmo utiliza uma **fila** para percorrer a árvore. A cada iteração, os nós de um nível são processados, seus valores são armazenados e seus filhos são adicionados à fila para o próximo nível. Esse processo é repetido até que todos os nós sejam visitados.

A saída é uma lista de listas, onde cada lista contém os valores dos nós de um nível específico da árvore. O algoritmo é eficiente e usa a estrutura de **BFS** para garantir a travessia da árvore de forma organizada e ordenada por níveis.




<p align="center">
  <img src="assets\102.png" alt="Print da Questão 102" width="600"/>
</p>    

---

## 🔹 Problema 3:   297. Serialize and Deserialize Binary Tree
**Nível:** Difícil  
**Implementação:** Código 3  

O problema exige a implementação de funções para **serializar** e **desserializar** uma árvore binária. A **serialização** é o processo de converter a árvore em uma string, de forma que ela possa ser armazenada ou transmitida, enquanto a **desserialização** reconstrói a árvore original a partir dessa string.

A estratégia utilizada é baseada em uma **traversal em largura (BFS)**. Para a serialização, percorremos a árvore nível por nível. A cada nó visitado, adicionamos seu valor à string e, quando encontramos um nó nulo (`None`), representamos com o marcador `"null"`. Isso nos permite capturar a estrutura completa da árvore, incluindo as ausências de nós. Durante a desserialização, a string gerada pela serialização é dividida em valores e, com base nessa sequência, reconstruímos a árvore. Usamos uma fila para garantir que a ordem dos nós seja preservada e, conforme iteramos sobre a lista de valores, recriamos os nós e suas conexões.

Por exemplo, para uma árvore com a entrada `[1,2,3,null,null,4,5]`, a serialização gera a string `"1,2,null,null,3,4,null,null,5"`. Durante a desserialização, essa string é convertida de volta na árvore original, com os valores atribuídos aos nós na mesma ordem.

O processo de serialização e desserialização é eficiente, com **complexidade de tempo O(n)**, onde `n` é o número de nós na árvore, pois cada nó é visitado uma única vez em ambos os processos. A **complexidade de espaço também é O(n)**, devido à armazenagem da string serializada e à fila utilizada na desserialização.



<p align="center">
  <img src="assets\297.png" alt="Print da Questão 297" width="600"/>
</p>    

---

## 🔹 Problema 4:   124. Binary Tree Maximum Path Sum
**Nível:** Difícil  
**Implementação:** Código 4  

O problema pede a implementação de duas funções: **serialização** e **desserialização** de uma árvore binária. A **serialização** converte a árvore binária em uma string, e a **desserialização** reconstrói a árvore a partir dessa string.

Na função de **serialização**, o objetivo é converter a árvore binária em uma representação textual. Para isso, utilizamos uma abordagem de **busca em largura (BFS)**, onde percorremos a árvore nível por nível. Em cada nó, registramos seu valor. Se o nó for `None`, registramos um marcador especial, como `"null"`, para indicar a ausência de um nó. Isso garante que a estrutura da árvore, incluindo os nós ausentes, seja preservada.

A função de **desserialização** tem a tarefa de reconstruir a árvore binária a partir da string gerada pela serialização. A string é convertida de volta para uma lista de valores, e, em seguida, a árvore é reconstruída usando esses valores na mesma ordem em que foram processados na serialização. Durante esse processo, se encontrarmos um valor `"null"`, sabemos que devemos atribuir `None` àquele nó, indicando a ausência de um nó.

Essa abordagem garante que a árvore original seja reconstruída exatamente da mesma forma após a serialização e desserialização. Ao utilizar uma busca em largura, a função é capaz de gerar uma string que reflete fielmente a estrutura da árvore, permitindo que a desserialização reconstrua a árvore corretamente.


<p align="center">
  <img src="assets\124.png" alt="Print da Questão 124" width="600"/>
</p>    

---

## Instalação
**Linguagem:** Phyton
**Framework:** Nenhum  

---

## Uso
Necessário compilador **Python 3 ou superior**.  
Exemplo para compilar o segundo problema:  

```bash
$ python level_order_traversal.py
$ python3 level_order_traversal.py

