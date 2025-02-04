# Operações Regulares

> Lembre que "Alfabeto" são todas as entradas que um autômato pode receber.<br>
> Por sua vez, "Linguagem", é o conjunto de todas as cadeias que a máquina M aceita.<br>

> Se A é o conjunto de todas as cadeiras que a máquina M aceita, que dizemos que A é a Linguagem da máquina M e escrevemos L(M) = A.

> Uma máquina sempre reconhece uma única linguagem.

Definimos algumas operações sobre linguagens, chamadas operações regulares, e as usamos para estudar propriedades de linguagens regulares.

---
## Operações Regulares

Sejam **A** e **B** linguagens. Definimos as operações regulares **união, concatenação e estrela** da seguinte forma:

**União**: A U B = {x | x E A ou x E B}

**Concatenação**: A . B = {xy | x E A e y E B}

**Estrela**: A* = {x1x2 ... xk | k >= 0 e cada xk E A}

A operação de união apenas pega todas as cadeias em ambas A e B e as junta em uma linguagem.

A operação de concatenação acrescente uma cadeia de A na frente de uma cadeia de B de todas as maneiras possíveis para obter as cadeias na nova linguagem.

A operação estrela é um pouco diferente das outras. Ela se aplica apenas uma única linguagem em vez de duas linguagens diferentes. Ou seja, a operação estrela é uma operação unária ao invés de uma operação binária. Ela funciona justapondo qualquer número de cadeias em A para obter uma cadeia na nova linguagem. Em razão de "qualquer número" incluir 0 como possibilidade, a cadeia vazia E é sempre um membro de A*, independentemente do que A seja.

![img01](https://github.com/user-attachments/assets/29ae08b2-7fda-45c4-91e6-28a15f151bc1)

---
## Propriedade do Fechamento

Seja Z = {..., -3, -2, -1, 0, 1, 2, ...} o conjunto dos números naturais. Quando dizemos que Z é fechado sob multiplicação, queremos dizer que, para quaisquer **x** e **y** em Z, o produto **x . y** também está em Z.

Em geral, uma coleção de objetos é fechada sob alguma operação se, aplicando-se essa operação a membros da coleção, recebe-se um objeto ainda na coleção. Mostraremos a seguir que a coleção de linguagens regulares é fechada sob as três operações regulares.

---
## Teoremas e Provas

**TEOREMA**: A classe de linguagens regulares é fechada sob a operação de união. Em outras palavras, se A1 e A2 são linguagens regulares, o mesmo acontece com A1 U A2.

**PROVA**: Temos as linguagens regulares A1 e A2 e desejamos mostrar que A1 U A2 também é regular. Em razão de A1 e A2 serem regulares, sabemos que algum autômato finito M1 reconhece A1 e algum autômato finito M2 reconhece A2. Para provar que A1 U A2 é regular exibimos um autômato finito (chame-o M) que reconhece A1 U A2.

Esta é uma prova por construção. Construímos M a partir de M1 e M2. A máquina M tem de aceitar sua entrada exatamente quando M1 ou M2 a aceitaria, de modo a reconhecer a linguagem da união. Ela funciona simulando ambas, M1 e M2, e aceitando se uma das simulações aceita.

Não podemos simular uma e depois a outra (simular M1 e depois M2, por exemplo). Precisamos construir uma máquina que simule ambas simultaneamente. 

Faça de conta que você é M. À medida que os símbolos de entrada chegam um por um, você simula ambas M1 e M2 simultaneamente. Os estados da máquina M serão o produto k1 x k2, sendo k1 os estados de M1 e k2 os estados de M2.

![img02](https://github.com/user-attachments/assets/19755448-c873-40ff-aa79-f3c2f9abf20a)<br>
![img03](https://github.com/user-attachments/assets/a071e053-bd8b-408c-89d1-ff3c3166629a)<br>
![img04](https://github.com/user-attachments/assets/d423dbec-17e6-4d9a-9d3f-e8d153ea5aab)<br>

---
