# Theremin

O theremin é um instrumento musical eletrônico controlado sem contato físico. O nome vem do seu inventor, Léon Theremin, que patenteou o dispositivo em 1928.

Nesse tutorial você fará uma versão to theremin usando a Franzininho.



#### Materiais necessários

* Franzininho
* 2 LDR
* BC548
* Resistor 330 R
* Alto falante 8 ohm

#### Circuito

![](../.gitbook/assets/theremin.png)

  


#### Código

O código a seguir ler o valor da entrada analógica e atua na saída do speaker

{% code-tabs %}
{% code-tabs-item title="Theremin" %}
```c
/*
 * Theremim Franzininho
 * Autor: Fábio Souza
 * Data: 10/09/2018
 */
int speaker = 0; // pino de saída do falante
int sensor = 1;
void setup()
{
 pinMode(speaker, OUTPUT);
}
// Theremin
void loop()
{
 digitalWrite(speaker, HIGH);
 delayMicroseconds(analogRead(sensor)<<2);
 digitalWrite(speaker, LOW);
 delayMicroseconds(analogRead(sensor)<<2);
}
```
{% endcode-tabs-item %}
{% endcode-tabs %}



### Vídeo



{% embed data="{\"url\":\"https://youtu.be/l1MmqiYB4GI\",\"type\":\"video\",\"title\":\"Faça um Theremin com a Franzininho\",\"description\":\"O theremin é um instrumento musical eletrônico controlado sem contato físico. O nome vem do seu inventor, Léon Theremin, que patenteou o dispositivo em 1928.\\n\\nNesse tutorial você fará uma versão to theremin usando a Franzininho.\\n\\nAcesse o tutorial completo em:\\n\\nhttps://franzininho.gitbook.io/franzininho-docs/exemplos/theremin\\n\\nSiga a Franzininho:\\n\\nFacebook: http://www.facebook.com.br/franzininho\\nInstagram: https://www.instagram.com/franzininho/\\nyoutube:\",\"icon\":{\"type\":\"icon\",\"url\":\"https://www.youtube.com/yts/img/favicon\_144-vfliLAfaB.png\",\"width\":144,\"height\":144,\"aspectRatio\":1},\"thumbnail\":{\"type\":\"thumbnail\",\"url\":\"https://i.ytimg.com/vi/l1MmqiYB4GI/mqdefault.jpg\",\"width\":320,\"height\":180,\"aspectRatio\":0.5625},\"embed\":{\"type\":\"player\",\"url\":\"https://www.youtube.com/embed/l1MmqiYB4GI?rel=0&showinfo=0\",\"html\":\"<div style=\\\"left: 0; width: 100%; height: 0; position: relative; padding-bottom: 56.2493%;\\\"><iframe src=\\\"https://www.youtube.com/embed/l1MmqiYB4GI?rel=0&amp;showinfo=0\\\" style=\\\"border: 0; top: 0; left: 0; width: 100%; height: 100%; position: absolute;\\\" allowfullscreen scrolling=\\\"no\\\"></iframe></div>\",\"aspectRatio\":1.7778}}" %}

