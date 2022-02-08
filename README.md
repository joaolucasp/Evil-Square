
# **Evil Square**

![screen1](https://user-images.githubusercontent.com/61102108/149201604-753d5483-a2d6-4dc5-9219-6dbf5616edc9.png)
![screen2](https://user-images.githubusercontent.com/61102108/149201609-097cff5d-5341-49a6-b91d-ae0dc6ed3f2f.png)


### Video explicativo
https://drive.google.com/file/d/15_XZWoxpiOITLKozNe7TU3F1zaieRQLu/view

## **Descrição**
> Fuja de soldados ao longo dos corredores do castelo de um Rei insano. <br> Este é um jogo singleplayer desenvolvido em assembly.
> <br>

## **História**
> A história do jogo se passa em um reino governado por um quadradado cruel.
Neste reinado havia um humilde e bondoso quadrado que cometeu um crime de desobediência ao rei. 
Então, ele foi levado ao castelo, acorrentado, preparado para o pior, pois ele sabia da maldade do rei.
Sem ser surpreendido, o mesmo foi setenciado a morte apenas para a satisfação do rei. Cansado das
injustiças ele recuperou suas forças e, de maneira inacreditável, quebrou as correntes e começou a fugir
para fora do castelo percorrendo metros intermináveis de um tapete aveludado de cor vermelha.


## **Como Jogar**
> Após inserir seu Nickname e dar Start no jogo, use as teclas WASD para se esquivar dos Evil's Square's e chegue até a linha de chegada! Conforme você for subindo de nível, novos oponentes surgirão e ficará mais difícil de vencer o jogo! Caso você não consiga se esquivar de um Evil Square, você perderá o jogo! Mas calme, é só apertar a tecla de jogar novamente que o jogo reinicia! <br>

## **Especificações Técnicas**
### 1) **Inicialização**

> ### **Main** <br> 
> Responsável pela inicialização de variáveis estáticas e chamada das funções principais. 

> ### **Menu** <br>
> Responsável pela primeira interação com o usuário, requisitando o nome.

> ### **Inicialização de variáveis** <br>
> Responsável pela inicialização de váriáveis a cada chamada de level.

---

### 2) **Lógica principal do jogo**
> ### **Level Up** <br> 
> Responsável pela verificação e chamada dos níveis.

> ### **Movimentação do Good Square** <br> 
> Responsável pela movimentação do Good Square. <br> 
> > Critério de parada:
> - Verificação com a linha de chegada;

> ### **Movimentação dos Evil's Squares** <br> 
> Responsável pela movimentação do Evil Square. <br> 
> > Critério de parada:
> - Verificação de colisão com o Good Square;
> > Cálculo de movimentação:
> - Movimenta-se na vertical, horizontal ou diagonais.
> - Verificação da posição de acordo com as coordenadas (x, y) do Good Square:
>   - Verificação da linha (Y);
>   - Verificação da coluna (X);

> ### **Game Over** <br> 
> Responsável pela impressão da tela de Game Over, perguntando se o usuário deseja jogar novamente.<br> 
> > Opção 1 (jogar novamente):
> - Volta para a função main;
> > Opção 2 (sair do jogo):
> - Chama a função EndGame;

> ### **End Game** <br> 
> Responsável por exibir as estatísticas da partida.<br> 

---

### **Observações de implementação:**

> ### **Delay** <br> 
> Tal função é responsável por fazer a interação entre o usuário e o jogo. Entretanto, é importante ressaltar que os valores implementados podem variar de ambiente para ambiente.  
> É provável que em sua máquina o jogo não rode corretamente, uma vez que os clocks do seu processador podem rodar em uma frequência superior (ou inferior)  à implementada. <br>
> Logo, é necessário adequá-la para seu computador. <br>
> Para isso, altere a seguinte linha de código:

/SquareZero.asm
<code>

    loadn r1, #2000
	
    Delay_volta2:
	    loadn r0, #3000
</code>

> - Quanto maior o valor, mais devagar as movimentações.

---
## **Esse projeto foi desenvolvido para a disciplina de Organização de Computadores Digitais (ICMC - USP)**
