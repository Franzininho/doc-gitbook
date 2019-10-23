---
title: Gravação do bootloader Gemma
---

# Gemma

## Gravação do bootloader Gemma

A Arduino Gemma, criada pela Adafruit, possui um bootloader próprio para o Attiny85. Você pode usar a Franzininho como uma Arduino Gemma gravando esse bootloader no Attiny85.

A seguir vamos apresentar o passo a passo para gravação do bootloader no Attiny85 e configuração dos drivers em seu computador.

## Materiais Necessários

* Arduino UNO
* Fios \(Jumpers\)
* Protoboard

## Circuito

Você precisará fazer a seguinte ligação do ATtiny85 no Arduino UNO:

![](../../.gitbook/assets/bootloarder-gemma-01.png)

## Preparando o Arduino UNO para programar o bootloader

A Adafruit disponibiliza um sketch para a [gravação do bootloader](https://learn.adafruit.com/introducing-trinket/repairing-bootloader) da Arduino Gemma e Trinket.

{% hint style="info" %}
Sketch – No mundo dos microcontroladores, “sketch” são programas ou parte de programas prontos que servem de “modelo” ou podem ser aplicados na íntegra nos microcontroladores, no bom estilo Copia e Colar.

Bootloader da Adafruit:

https://learn.adafruit.com/introducing-trinket/repairing-bootloader  
{% endhint %}

Para nosso tutorial, vamos usar uma versão traduzida pelo Mau Maker. Você pode acessar o projeto disponibilizado na [plataforma Arduino Create](https://create.arduino.cc/editor/maujabur/397f14ad-1fc1-49a5-b9a8-2143fda15b35/preview).

Você também pode baixar os arquivos que estão nesse repositório e gravar usando a IDE Arduino offline.

{% hint style="info" %}
Caso não tenha IDE do Arduino \(ambiente de programação\) , acesse www.arduino.cc
{% endhint %}

O primeiro passo é fazer o upload do código para a Arduino UNO.

Com as ligações feitas corretamente para a gravação do bootloader, abra o terminal serial, configure o baudrate para 9600 bps, e envie a letra G para iniciar a gravação. Será exibida a seguinte mensagem:

![](../../.gitbook/assets/bootloarder-gemma-02.png)

Após a gravação do microcontrolador, você poderá retirá-lo da matriz de contatos e colocá-lo na Franzininho, mas lembre-se de colocar na posição correta.

