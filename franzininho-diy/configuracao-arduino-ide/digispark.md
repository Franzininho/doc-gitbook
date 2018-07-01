---
title: Configuração da IDE Arduino para programar Digispark
---

# Digispark

Com o microcnucleus gravado no Attiny85 você pode programar a franzininho usando o pacote de software desenvolvidos para a digispark. Para isso, você precisa instalar o pacote de suporte da Digispark na IDE Arduino \(É necessário estar conectado a internet\).

Acesse o menu Arquivos-&gt;preferencias e cole a URL a seguir para gerenciador de placas:

```text
http://digistump.com/package_digistump_index.json
```

![url](../../.gitbook/assets/image1.PNG)

Agora acesso o menu: Ferramentas-&gt; placa -&gt; Gerenciador de placas. Aguarde alguns segundos até atualização da lista de pacotes e digite "digi". Aparecerá o pacote “Digistump AVR Boards” e clique em instalar.

![instalar](../../.gitbook/assets/image2.PNG)

Aguarde o fim da instalação e clique em fechar.

Agora acesse o menu: Ferramentas-&gt;placas e escolha a opção “Digispark \(Default - 16.5mhz\)”.

![select board](../../.gitbook/assets/image3%20%284%29.png)

Agora acesse o menu Ferramentas-&gt; programador e selecione a opção Micronucleus:

![micronucleus](../../.gitbook/assets/image4%20%281%29.png)

Pronto a IDE está pronta para programar a placa.

