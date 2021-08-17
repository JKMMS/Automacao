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

- Pode-se medir vazão em um líquido através do sistema de placa de orifício, onde a vazão pode ser calculada pela expressão
abaixo, sendo Q dado em m3/s:
Q = C.Ao.v(2.(p1-p2)/d)
Elabore uma função que, a partir dos valores
fornecidos, calcule a vazão. Os valores de p2 e p1 são
as entradas da função, Q é a saída e os demais termos são constantes da função. Teste
esta função através de um programa, com os seguintes valores:
C= 0,68
d= 1000,00 kgf/m3
diâmetro do orifício :29,75 mm => Ao
p1 = 201,00 kPa
p2 = 154,00 kPa (Q=144,92x10-6m3/s)
Agora, utilize as duas entradas analógicas do CP como entradas dos valores de pressão,
com fundo de escala de 20.000, correspondendo a 200,00 kPa. Apresente os valores das
pressões, em kPa, e a vazão calculada, em m3/s (com precisão máxima) e em l/m, na tela
da IHM. (demais valores com dois algarismos significativos após a vírgula)

- [x] Fazer a função para calcular a vasão

- [x] Testar se está funcionando com o valor do sor

- [ ] Fazer funcionar quando P2 for maior que P1 e der um valor negativo na raiz

### Exercício 11

- Crie uma estrutura de dados que armazene o valor obtido por um determinado tipo de sensor, o valor de saída da variável
medida convertido na escala, o fator de conversão de escala, limites máximo e mínimo para o valor desta variável e dois sinais 
booleanos indicando alarme de mínimo e alarme de máximo. Elabore um bloco funcional que calcula o valor de saída a partir do 
valor do sensor dado (lendo a entrada analógica, tensão de 0,00V a 10,00V), e atualize os alarmes de máximo e mínimo. 

Crie um array com 10 elementos desta estrutura. Os limites de máximo e mínimo em cada elemento são aleatórios e de sua escolha. 
Elabore um programa que processe estes dados através do bloco funcional elaborado (que possa processar cada um dos sensores, de
1 a 10), e onde possa ser escolhido, através da IHM, qual o sensor terá seus dados processados e exibidos na tela.

### Exercício 12

- Desenvolver um sistema de gerenciamento de uma bomba de circulação de produto químico, em três tanques.

Existe um LSH (sensor de nível alto) e um LSL (sensor de nível baixo) para cada tanque. 6VAR

Para ligar a bomba (K2), nenhum dos tanques deve estar com o nível alto e o operador deve dar partida por um botão B1, podendo desligá-la pelo botão B2. 
Se o nível dentro de um dos tanques subir ao limite superior, a bomba desliga. 

Se o nível de um dos tanques atingir o limite mínimo, e nenhum dos outros tanques estiver no limite máximo, deve ser ligada a bomba K2 
e ligada a saída de alarme visual e sonoro (K1), ficando esse alarme ativo por 5 segundos . 

Crie uma estrutura para de dados para os tanques, contendo uma variável de medição do nível de concentração do produto (REAL) e duas 
variáveis de contagem (INT) dos eventos de nível máximo atingido, nível mínimo atingido (ambos de cada tanque), e de acionamentos da bomba (do sistema), 
crie um array contendo as estruturas de dados dos três tanques. 

A leitura de concentração para os três tanques é feita por sensores/transmissores analógicos (AT) que utilizam uma única entrada analógica (valor de 0,00UI 
a 50,00UI, fundo de escala 10.000) selecionada a cada 5 segundos para a leitura de cada tanque e respectiva atualização do dado no array de tanques 
(intervalo de 5s, mede tanque 1, intervalo de 5s, mede tanque 2, intervalo de 5s, mede tanque 3, e assim sucessivamente). 

Exibir na tela principal da IHM o status da bomba, do alarme e da medição atualizada dos três tanques), em uma segunda tela, exibir os contadores de eventos 
atualizados dos três tanques. Ao ser reiniciado o CLP, todas as variáveis retornam ao valor inicial “zero”.







Trabalho de **Automação** da *Fundação __Liberato__*
