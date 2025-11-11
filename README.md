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

Dado a raiz de uma árvore binária de busca (BST), o objetivo é balancear a árvore para garantir que a diferença de altura entre as subárvores de cada nó não seja maior que 1, e retornar a raiz da árvore balanceada.

Para balancear a árvore, primeiro realizamos uma **travessia in-order**, onde percorremos a árvore e criamos uma lista com os valores dos nós em ordem crescente. A partir dessa lista ordenada, reconstruímos a árvore binária de busca, escolhendo o valor do meio da lista como a raiz. Isso garante que a árvore seja balanceada, pois ao escolher o meio da lista, dividimos a árvore igualmente em subárvores esquerda e direita. Repetimos esse processo para as subárvores esquerda e direita até que todos os nós estejam na nova árvore balanceada.

A função **inorder** realiza a travessia in-order e retorna os valores dos nós ordenados. A função **sortedArrayToBST** cria uma árvore balanceada a partir dessa lista ordenada, e a função **balanceBST** utiliza essas funções para balancear a árvore e retornar a nova raiz balanceada.

A complexidade do tempo é O(n), onde n é o número de nós, pois percorremos todos os nós da árvore para realizar a travessia e reconstruir a árvore balanceada. O espaço é O(n), devido à lista auxiliar que armazena os valores e à pilha de chamadas recursivas.



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

