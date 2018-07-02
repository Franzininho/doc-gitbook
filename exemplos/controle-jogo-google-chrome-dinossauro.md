# Controle Jogo Google Chrome \(dinossauro\)

## Controle para o Jogo do Google Chrome \(dinossauro\) com a Franzininho

Nesse tutorial vamos fazer um controle para jogar o jogo do Google Chrome, aquele do dinossauro que aparece quando a internet cai :\).

Para esse tutorial você precisa instalar o bootloader Micronucleus, conforme exibido no [tutorial de gravação do bootloader Micronucleus](https://github.com/Franzininho/franzininho-docs/tree/master/02-Franzininho-DIY/Gravação%20do%20bootloader/Micronucleus)

### Circuito

Para esse projeto você irá precisar apenas de uma Franzininho e uma chave tactil:

![url](../.gitbook/assets/controle-jogo-google-chrome-dinossauro_circuito.png)

### Configuração da IDE Arduino

Vamos usar os exemplos da Digispark para USB. Para isso, você precisa instalar o pacote de suporte da Digispark.

Acesse o menu Arquivos-&gt;preferencias e cole a URL a seguir para gerenciador de placas:

```text
http://digistump.com/package_digistump_index.json
```

![](../.gitbook/assets/controle-jogo-google-chrome-dinossauro_image1.PNG)

Agora acesso o menu: Ferramentas-&gt; placa -&gt; Gerenciador de placas. Aguarde alguns segundos até atualização da lista de pacotes e digite "digi". Aparecerá o pacote “Digistump AVR Boards” e clique em instalar.

![instalar](../.gitbook/assets/controle-jogo-google-chrome-dinossauro_image2.PNG)

Aguarde o fim da instalação e clique em fechar.

Agora acesse o menu: Ferramentas-&gt;placas e escolha a opção “Digispark \(Default - 16.5mhz\)”.

![select board](../.gitbook/assets/controle-jogo-google-chrome-dinossauro_image3.png)

Agora acesse o menu Ferramentas-&gt; programador e selecione a opção Micronucleus:

![micronucleus](../.gitbook/assets/controle-jogo-google-chrome-dinossauro_image4.png)

Pronto a IDE está pronta para programar a placa.

## Sketch

Para o funciomento da Franzininho como controle do jogo do Google Chrome \(dinossauro\), você precisa carregar o seguinte sketch:

```cpp
#include "DigiKeyboard.h"         //biblioteca da digispark para teclado

const int btPin = 2;          //pino que a tecla esta ligada

int estadoAnteriorBotao = 0;   // armazena o estado anterior do botão


void setup() {
  pinMode(btPin,INPUT_PULLUP);    //configura o pino do botão como entrada com pullup habilitado
}


void loop() {

  int estadoAtualBT= digitalRead(btPin);      // Lê estado do botão


  if ((estadoAtualBT != estadoAnteriorBotao)&& (estadoAtualBT == LOW)){       //Se o botão foi pressionado e o seu estado mudou

  //Envia comando da tecla espaço para o computador

  DigiKeyboard.sendKeyStroke(0);
  DigiKeyboard.println("  ");

  }

  estadoAnteriorBotao = estadoAtualBT;  //salva o estado do botão para comparar na próxima leitura

}
```

Pronto, agora é só se divertir.

Confira o vídeo de funcionamento:

{% embed data="{\"url\":\"https://www.youtube.com/watch?v=aMfCYi9xhcA\",\"type\":\"video\",\"title\":\"Controle para o Jogo do Google Chrome \(Dino\) com a Franzininho\",\"description\":\"Quando você ficar sem internet que tal pegar a sua Franzininho, um botão e jogar o joguinho do dinossauro do Google Chrome?\\n\\nConfira o tutorial completo no github da \#Franzininho: http://bit.ly/2EszCXS\\n\\nCompartilhe com seus amigos e siga a Franzininho.\\n\\nMaterial colaborativo para oficinas\(colabore\): https://goo.gl/RXjure\\nDocumento para criticas e sugestões: https://goo.gl/H5hWgi\\nFlipsnack:https://www.flipsnack.com/FBA58CB9E8C/\\n\\nGrupos de discussão:\\nGrupo no Facebook: https://www.facebook.com/groups/29923...\",\"icon\":{\"type\":\"icon\",\"url\":\"https://www.youtube.com/yts/img/favicon\_144-vfliLAfaB.png\",\"width\":144,\"height\":144,\"aspectRatio\":1},\"thumbnail\":{\"type\":\"thumbnail\",\"url\":\"https://i.ytimg.com/vi/aMfCYi9xhcA/maxresdefault.jpg\",\"width\":1280,\"height\":720,\"aspectRatio\":0.5625},\"embed\":{\"type\":\"player\",\"url\":\"https://www.youtube.com/embed/aMfCYi9xhcA?rel=0&showinfo=0\",\"html\":\"<div style=\\\"left: 0; width: 100%; height: 0; position: relative; padding-bottom: 56.2493%;\\\"><iframe src=\\\"https://www.youtube.com/embed/aMfCYi9xhcA?rel=0&amp;showinfo=0\\\" style=\\\"border: 0; top: 0; left: 0; width: 100%; height: 100%; position: absolute;\\\" allowfullscreen scrolling=\\\"no\\\"></iframe></div>\",\"aspectRatio\":1.7778}}" %}

## Desafio

Você percebeu que o jogo precisa de mais um comando para o dinossauro baixar? Insira esse comando incluindo uma nova tecla.

## Crie novos projetos

O exemplo apresentado pode ser adaptado para controle de outros jogos que usam teclas como controle. Verifique quais jogos você pode controlar e insira mais teclas.

Boa diversão

