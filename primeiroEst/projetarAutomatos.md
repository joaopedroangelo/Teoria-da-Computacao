# Projetar Autômatos Finitos

> Tente se colocar no lugar do autômato<br>
> Você recebe uma sequência de caracteres como entrada e vai vendo os símbolos na cadeia um por um. Depois de cada símbolo você tem que decidir se a cadeia vista até então está na linguagem (ou seja, se é aceita).

---
## Exemplo 01

Suponha que o alfabeto de sua máquina seja {0, 1} e a linguagem consista de todas as cadeias com um número ímpar de 1s.

Você deseja construir um autômato finito E1 para reconhecer essa linguagem. Fazendo de conta que é o autômato, você começa obtendo uma cadeia de entrada de 0s e 1s, símbolo a símbolo.

Você não precisa lembrar da cadeia inteira. Simplesmente lembre apenas se o número de 1s visto até agora é ímpar ou par. Se você ler um 1, inverta a resposta. Mas se ler um 0, mantenha a resposta atual.

Assim, você tem uma máquina com dois estados (par e ímpar). Desenhe os estados.

Em seguida, você atribui as transições, vendo como ir de uma possibilidade para outra ao ler um símbolo.

![01](https://github.com/user-attachments/assets/a03be85d-b4e9-4099-b2a1-7fd512902af7)

Em seguida, você pensa no estado inicial. O estado inicial será aquele que aceita a cadeia vazia. Faça com que o estado "ímpar" seja o estado de aceitação.

![img02](https://github.com/user-attachments/assets/57bef16a-2389-4cd9-b4d2-9897b880dc1a)

---
## Exemplo 02

Este exemplo mostra como projetar um autômato finito E2 para reconhecer a linguagem regular de todas as cadeias que contêm a cadeia 001 como uma subcadeia.

Por exemplo, 0010, 1001, 001 e 1111110011110 estão todas na linguagem, mas 11 e 0000 não estão.

Como você reconheceria esta linguagem se estivesse fazendo de conta ser E2? À medida que os símbolos chegassem, você saltaria sobre todos os 1s. Se você chegar num 0, então nota que viu o primeiro dos três símbolos do padrão 001. Se nesse ponto você vê um 1, volta volta a saltar sobre os 1s. Mas se vê um segundo 0, você deve lembrar que já viu dois 0. Agora você simplesmente precisa continuar fazendo essa varredura até ver a sequência correta.

Se você encontrar a cadeia que busca, lembre-se que já está no estado de aceitação e continue nele lendo todos símbolos da cadeia.

Desenha os estados (q, q0, q00, q001).
Monte as transições.
Verifique o estado de aceitação.
Verifique o estado inicial.

![img03](https://github.com/user-attachments/assets/1f577a2c-5d88-4f44-9abe-d36f5d2baa5f)
