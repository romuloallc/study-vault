Subject: [[Network]] #network
Type: [[YouTube]] #youtube
From: 
- [[Gustavo Kalau]] - https://www.youtube.com/watch?v=MSEhqtKNYzo

[[MTU - Maximum Transfer Size]] - default 1500 bytes (Camada 2 - enlace - Frame)

Cabeçalho de camada 3 (Redes) - IPv4 ocupa 20 bytes - IPv6 ocupa 40 bytes
Cabeçalho de camada 4 (Transporte)- TCP ocupa 20 bytes - UDP ocupa 8 bytes  

Payload: Carga útil/informação
1500 B de MTU, utilizando IPv4 e TCP - temos no máximo 1460 B de payload, também chamado de [[MSS - Maximum Segment Size]]

É possível alterar o MTU, por exemplo, para 9000 Bytes.
Utilizando IPv4 e TCP - temos no máximo 8960 B de MSS
Com isso temos menos pacotes, menos overhead, maior utilização do link, menos ciclos de CPU dos dispositivos finais.

É viável em qualquer tipo de tráfego? Normalmente não, somente em casos de backup, storage, arquivos grandes, bancos de dados.

Como a rede se comporta quando tem dispositivos intermediários que não estão preparados para receber ou não suportam o Jumbo Frame?

No IPv4, o dispositivo intermediário de camada 3 pode fragmentar o Frame original em Frames menores em vez de descartá-lo. Dispositivos intermediários IPv6 não fragmentam Frames por padrão.

[[ICMP Path MTU Discovery]] (Camada 3 - Rede)- Frames com MTUs com o bit DF (Don't Fragment) ativado, isso não permite que dispositivos intermediários fragmentem o tráfego. O dispositivo vai mandando sondas (probes),caso o dispositivo intermediário precisar fragmentar, não vai conseguir  e vai responder com uma mensagem de erro do ICMP e a máquina vai encaminhar o trafego com o MTU correto 

Dispositivos intermediários de Camada 2 (Enlace), não tem ICMP Path MTU DIscovey, logo será descartado. As camadas superiores (TCP), não terão a confirmação que o segmento foi recebido e irá retransmitir o segmento ajustando o MSS até que tenha confirmação (Dividindo o MSS por 2 até passar e depois irá aumentando novamente (TCP Slow-Start)) assim gera oneração da rede.



---
[[ICMP - Internet Control Message Protocol]]