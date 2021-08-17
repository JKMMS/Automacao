# Exercícios de Automação - Lista de ST

## Afazeres

### Exercício 1

- Três cargas devem ser acionadas em sequência, comandadas por um único botão. A cada toque no botão, uma das cargas é acionada. Um segundo
botão realiza o desligamento das cargas. Elabore um programa que realize este acionamento. Utilize o FUNCTION Block R_TRIG para a detecção 
de borda DO botão.

- [x] Feito e funcionando certinho com IHM

### Exercício 2

- Elabore um acionamento sequencial de três cargas usando um botão. A segunda carga aciona 5s após a primeira carga ser acionada, e a terceira
5s após a segunda. Implementar um botão de desligamento das cargas.

- [x] Feito e funcionando certinho com IHM

### Exercício 3

- A lixa de uma lixadeira de fios deve ser afiada periodicamente, e para isto o sentido de rotação do motor deve ser invertido.
Para isto, o controle possui duas saídas digitais, uma que aciona a o motor no sentido de lixamento, outra que aciona o motor 
no sentido de afiação. O painel de operação possui um botão de partida e um botão de parada apenas para operação de lixamento,
e o painel de manutenção possui um botão  de afia e um de parada de emergência que atua nos dois modos (lixamento e afiação). 
(todos são entradas digitais do CP). O eixo da máquina  possui um sensor de rotação (uma entrada digital do CP, será simulada 
manualmente), que indica se o eixo está girando (#1) ou parado (#0). A  lógica de acionamento dita que o motor só pode ser 
acionado quando seu eixo estiver parado. Caso seja comandado para trocar de direção com o  eixo em movimento, o comando deve 
efetuar o desligamento do movimento e aguardar novo comando somente quando o eixo estiver parado. Elabore um  programa que 
implemente esta lógica. No display da IHM devem ser exibidos o status do motor (‘OPERAÇÃO’ ou ‘AFIAÇÃO’), DO sensor de rotação 
(‘MOTOR GIRANDO’ ou ‘MOTOR PARADO’).

A lógica do exercício foi alterada um pouco na hora de desenvolver o programa pois o enunciado estava bastante confuso.

- [x] A lixadeira só afia se os botões de PARTIDA e AFIAR estiverem pressionados

- [x] A lixadeira só lixa quando os botões de PARTIDA e LIXAR estiverem pressionados

- [x] A lixadeira para totalmente e espera o próximo comando quando pressionado o botão de PARADA

- [x] A lixadeira para totalmente ao ser pressionado o botão de EMERGÊNCIA

- [x] Feito e funcionando certinho com IHM

### Exercício 4

- Elabore um comando liga-desliga para uma bomba de enchimento de um reservatório utilizando um sensor de nível (0,00V a 10,00V) em uma entrada
analógica. Acione a bomba (saída digital) quando a tensão de entrada for igual ou inferior a 30%% do valor máximo da entrada e desligue a bomba 
quando a tensão de entrada for igual ou superior a 70% do valor máximo. A IHM deve exibir as mensagens ‘NIVEL BAIXO’, ‘NIVEL NORMAL’ E ‘NIVEL 
ALTO’ DE ACORDO com os o valor do sensor comparado com os limiares percentuais. Caso um botão do painel (entrada digital), denominado emergência,
seja acionado, a carga deve ser desligada e não pode ser acionada por um período de 5 segundos. O valor máximo deve ser editado pela IHM 
(entrada de texto), e salvo em uma variável de programa não volátil através de um botão da IHM. O valor de tensão da medição de nível, e do 
valor máximo também devem ser exibidos no display da IHM

- [x] Acionar a bomba com uma tensão abaixo de 30%

- [x] Desligar a bomba com uma tensão acima de 70%

- [x] Fazer o botão de emergência

- [] Adicionar o tempo de 5 segundos que a bomba não pode ser acionada após pressionado o botão de emergência



Trabalho de **Automação** da *Fundação __Liberato__*
