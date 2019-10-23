---
description: Configuração da IDE Arduino para programar Digispark
---

# Digispark

Com o micronucleus gravado no Attiny85 você pode programar a franzininho usando o pacote de software desenvolvidos para a digispark. Para isso, você precisa instalar o pacote de suporte da Digispark na IDE Arduino \(É necessário estar conectado à internet\).

Acesse o menu Arquivos-&gt;Preferências e cole a URL a seguir para gerenciador de placas:

```text
http://digistump.com/package_digistump_index.json
```

![url](../../.gitbook/assets/digispark-01.PNG)

Agora acesse o menu: Ferramentas-&gt; Placa -&gt; Gerenciador de placas. Aguarde alguns segundos até atualização da lista de pacotes e digite "digi". Aparecerá o pacote “Digistump AVR Boards” e clique em instalar.

![instalar](../../.gitbook/assets/digispark-02.PNG)

Aguarde o fim da instalação e clique em fechar.

Agora acesse o menu: Ferramentas-&gt;Placa e escolha a opção “Digispark \(Default - 16.5mhz\)”.

!\[select board./digispark-03.png\)

Agora acesse o menu Ferramentas-&gt; Programador e selecione a opção Micronucleus:

![micronucleus](../../.gitbook/assets/digispark-04.png)

Pronto a IDE está pronta para programar a placa.

