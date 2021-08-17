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

- [x] Adicionar o tempo de 5 segundos que a bomba não pode ser acionada após pressionado o botão de emergência

### Exercício 5

- Faça um programa para inverter uma string dada (armazenar em outra variável, a variável original deve permanecer inalterada).
Observação:a string deve poder ser modificada, como sendo uma constante do programa. Para o tamanho variável, use a função LEN.
Execute e apresente apenas em modo de simulação no Mastertool IEC

- [x] Inverter a frase

- [x] Fazer IHM e comentários

### Exercício 6

- A iluminação de uma sala é comandada em 3 pontos diferentes, através de interruptores. Desenvolva um programa que, a cada
alteração do estado de um dos interruptores, troque o estado da lâmpada, ou seja, cada vez que um dos interruptores é ligado
ou desligado, a lâmpada acende se estava apagada, ou apaga se estava acesa

- [x] Inverter o estado da lâmpada a cada toque no interruptor

- [x] IHM e comentários

### Exercício 7

- A saída de veículos normalmente é sinalizada por duas lâmpadas, que piscam alternadamente. Elabore um programa que realize
esta função, a partir da ativação de um sensor de porta de garagem aberta (entrada digital, #0: porta fechada, #1: porta 
aberta). Ao ser fechada a porta, as lâmpadas permanecem piscando por 5 segundos. Utilize uma frequência de piscada de 2 HZ.

- [x] Fazer as lâmpadas piscarem em 2Hz

- [x] Fazer as lâmpadas começarem a piscar quando a porta abre

- [x] Fazer as lâmpadas piscarem por mais 5 segundos depois que a porta fecha e depois desligarem

- [x] Fazer comentários e IHM

### Exercício 8

- Um fulão processa o couro através do seguinte procedimento: A partir de um botão de início (entrada digital):
- [x] Inicialmente, preenche-se o fulão com o produto de curtimento, através da válvula VPC.
- [x] O motor é acionado no sentido horário, através da saída MH por um tempo THC.
- [x] O motor é acionado no sentido anti-horário, através da saída MAH, por um tempo TAHC.
- [x] O fulão é esvaziado, através da válvula VD.
- [x] O fulão é preenchido com água, através da válvula VL.
- [x] O motor é acionado no sentido horário, através da saída MH por um tempo THL.
- [x] O motor é acionado no sentido anti-horário, através da saída MAH, por um tempo TAHL.
- [x] O fulão é esvaziado, através da válvula VD.
- [x] É sinalizado, através de uma lâmpada FP, o final do processo.
- [x] Exercício finalizado e funcionando certinho, com comentários e IHM
Após o ciclo completo, o sistema deve ficar pronto para ser acionado novamente. O nível alto do fulão é indicado pela chave de
nível NVC, e o nível baixo (vazio) é indicado pela chave NVV. Elabore um programa que realize este procedimento, com os 
seguintes tempos para simulação: THC =TAHC= 5s. THL=TAHL=8s
Cada fase do processo deve ser devidamente apresentada na tela da IHM através de uma variável de texto.


### Exercício 9

- Em um estacionamento duas células fotoelétricas distanciadas de 1.5 metros servem para identificar a entrada e saída de
carros. Quando a célula A é acionada primeiro que a célula B é porque um veículo está entrando. No caso contrário, um veículo 
está saindo. Se após uma das células ter seu facho de luz bloqueado, a outra não for interrompida, isto significa que uma pessoa
está passando e o evento deve ser ignorado. Caso o veículo pare diante das duas células e reverta o movimento, não deve haver 
alteração na contagem. A variável CONTA_VEICULOS indica o número de veículos no estacionamento. Desenvolva um bloco funcional 
que tenha como entrada a leitura dos sensores fotoelétricos (booleanos) e como saída a contagem de carros na garagem, o número 
de vagas disponíveis, a sinalização de um semáforo vermelho caso o número de vagas seja igual a MAX_VAGAS, uma constante do 
programa, e a sinalização de um semáforo verde caso o estacionamento esteja vazio. Utilize a tela da IHM para mostrar as
informações.

- [x] Fazer a lógica para verificar a entrada de carros

- [x] Fazer o contador de carros

- [x] Fazer o contador de vagas

- [x] Fazer a lógica para ignorar pessoas que passam pelo sensor

- [x] Fazer comentários e IHM

### Exercício 10

- 





Trabalho de **Automação** da *Fundação __Liberato__*
