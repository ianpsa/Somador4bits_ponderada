## Atividade Ponderada de programação: Somador de 4 bits

No que se diz respeito ao somador, o processo de criação deste aparato requeriu de mim alguns conhecimentos prévios. Claro, todos eles abordados nos auto-estudos e aulas, sendo estes: Portas lógicas (conjuntos de transistores), Representações numéricas (base 2 para base 10) e a partir destes conhecimentos conectei com o que estou aprendendo externamente referente à assembly, principalmente quando se fala de registradores e o famoso pointer (Esta parte gostaria de adicionar mais como curiosidade para acrescentar em relação à minha jornada para criar este somador básico).

---
### Etapa 1: Half adders

A partir dos autoestudos depreendi a lógica por trás dos somadores de bits, neste caso os half adders, a lógica se dá através do uso de uma porta XOR e uma AND, a XOR por si só já faz o papel da soma de dois bits, enquanto a porta AND trata o Cout (Valor tido quando se excede o valor máximo daquele somador). Entretanto com half adders ainda há um problema, apesar de tratarmos o Cout ainda não há como colocá-los em série pois não há espaço para contabilizar este Cin.

---
### Etapa 2: Full Adder

Na imagem abaixo já há um tratamento em relação ao Cin, ali é possível ver a partir das portas lógicas que este é somado em uma casa binária a mais com os próximos números na soma a partir de uma porta XOR, a funcionalidade é quase a mesma. o tratamento do Cout ainda é feito, tanto na contabilização do Cin quanto na soma dos bits, pois deve-se levar em conta o valor anterior, utilizam-se portas AND para contabilizar se há Cin quando as duas são 1 é verificado pela porta abaixo (OR) e então contabiliza-se um carry-out. Nesta etapa já temos a soma completa de um bit com carry-out e contabilização de Carry-in's.

<div align="center">
<image src="assets/somadorCompletoSolo.png">
</div>

---

### Etapa 3: O somador

Creio que agora você já saiba como vou chegar (é claro, você quem dá esta aula), com um somador de um bit completo podemos ligar os carry-in nos carry-outs dos anteriores, e assim temos mais possibilidades de bits que podem ser somados! Abaixo está a representação deste circuito completo no *Digital*.

<div align="center">
<image src="assets/somador4bits.png">
</div>

Na imagem podemos verificar que a conexão dos Cin e Couts está em série, ou seja o próximo somador sempre contabilizará quando o anterior "estourar. Vendo da direita para a esquerda o circuito podemos verificar que o primeiro bit da direita é o menos significativo e os posteriores à esquerda são os mais significativos como na comparação entre unidades, dezenhas, centenas e assim por diante, Neste caso não tratam-se de dezenas, centenas na base 10 mas sim outros bits que podemos adicionar à soma. Cada somador tem 3 entradas, um Cin, número X e Y a serem somados junto ao Cin, e um Cout, resultado do valor excedido da Soma. Por cada Somador representar um bit diferente da soma, separamos o cabeamento desta forma na imagem de forma à demonstrar os dois números de 4 bits na base 2 à serem somados.

---
### Simplificação e adição de display

Certo, agora que já somei os 4 bits, vou demonstrar o circuito simplificado, além disso adicionei mais dois displays para mostrar os valores de entrada e o de saída na base 10.

<div align="center">
<image src="assets/Somador4bits_simplificado.png">
</div>

Peguei a dica do distribuidor com um colega de classe para não ter que adicioanar manualmente cada parte do somador em cada parte do display de maneira tão bagunçada, este é o produto final, fruto de todas as etapas de aprendizado acima! Caso haja alguma dúvida sobre o meu desenvolvimento me contate que posso saná-la! Valeu prof!

Pontos de melhora: 
- Adicionar Distribuidores e memória para salvar valores em locais específicos de memória
- Adicionar Subtração
- Adicionar Multiplicação

---

### Vídeo Explicativo:


https://github.com/user-attachments/assets/70a679a2-4c7c-4aaf-b6e9-e158d05dc87e

