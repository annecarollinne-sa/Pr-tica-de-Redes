# Prática de Redes
Atividade prática de redes realizada no software Packet Tracer da Cisco

Gostaria de compartilhar um pouco do aprendizado sobre o funcionamento de uma rede hierárquica através da atividade realizada no Packet Tracer. 
A topologia está organizada em três camadas: Acesso, Distribuição e Núcleo.

<img width="1901" height="1007" alt="Captura de tela 2026-08-16 225139" src="https://github.com/user-attachments/assets/9714ee97-d7e5-4711-ab49-88144a8622b2" />
<br>
<br>
Na simulação ilustrada pela imagem, o **PC-Lab01**, pertencente à camada de acesso, origina um pacote ICMP destinado ao **Roteador-Core-4331**. O pacote é inicialmente encaminhado pelo **SW-Acesso-Lab**, que conecta os dispositivos finais à infraestrutura de rede. Em seguida, o tráfego é encaminhado ao **SW-Distribuição-3650**, responsável pela agregação dos switches da camada de acesso e pelo encaminhamento do tráfego em direção à camada de núcleo. Por fim, o pacote chega ao **Roteador-Core-4331**, localizado na camada Núcleo.

Após o recebimento do pacote pelo roteador, é enviada uma resposta ICMP ao dispositivo de origem, percorrendo o caminho inverso: 
**Roteador-Core-4331 → SW-Distribuição-3650 → SW-Acesso-Lab → PC-Lab01**.
Ao final da simulação, o Packet Tracer indica o status "Successful", demonstrando que a comunicação ICMP foi realizada com sucesso entre o PC-Lab01 e o roteador.

A atividade permite visualizar, na prática, a função de cada camada da arquitetura hierárquica: a **camada de Acesso** conecta os dispositivos finais, a **camada de Distribuição** agrega e encaminha o tráfego proveniente da camada de acesso, e a **camada Núcleo** fornece o encaminhamento do tráfego entre os diferentes segmentos da infraestrutura.

Obs.: Como curiosidade, esse tipo de comunicação utiliza o protocolo ICMP, o mesmo protocolo utilizado pelo comando ping para testar a conectividade entre dispositivos em uma rede. No caso do ping, são enviadas mensagens ICMP Echo Request e ICMP Echo Reply, permitindo verificar se o dispositivo de destino está acessível e se há resposta à comunicação.
