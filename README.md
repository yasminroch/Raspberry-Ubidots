# Descrição do projeto

Este projeto tem como objetivo uma comunicação que utiliza o protocolo MQTT(mensagem de diferentes clientes) com a plataforma Ubidots que disponibiliza um front-end em formato de dashboard para plotar dados obtidos a partir do sensor LDR. O sistema construído é composto pelo Raspberry Pi Pico e pelo sensor LDR, a montagem completa com o sistema funcionando pode ser encontrada [aqui](https://docs.google.com/document/d/1sURvk0v_3GZwNuWWNccdlO1JF08y88W_BfR49s-D6c4/edit?usp=sharing), porém, no tópico referente a “montagem” será tratado disso de maneira resumida.


# Montagem
Raspberry Pi Pico W;
Sensor de Luz Dependente de Resistor(LDR);
LED;
Resistor 220ohm e 100ohm;
Fios macho-macho;
Protoboard;
Cabo SBC.
IDE Thonny

# Pinos utilizados
Pino analógico(28):
Esse pino foi utilizado devido ao fato do LDR fazer leitura com mais precisão, diferente do digital. É recomendado utilizar o pino analógico do módulo ao medir a variação da luminosidade(que neste caso é feito pelo LDR);
Fonte de alimentação(3v3):
Onde o LDR está conectado, usado para obter a variação da luz;
GND:
Conectado pelo fio terra, é a referência de tensão;
Pino para LED(15):
Onde é conectado com o LED para fornecer iluminação ao ambiente.

 
# Conexão via protocolo MQTT e Ubidots
Foi utilizado a biblioteca umqtt.simple na IDE Thonny, para manter a conexão, o meio utilizado foi o Wi-fi, além disso, para conectar ao Ubidots, foi feito o uso do Broker, que são configurações MQTT do Ubidots que a própria plataforma oferece. Ou seja, é criado uma variável em devices e é usado o TOPIC que será o nome do dispositivo no Ubidots.




# Resultados
Ao obter sucesso na conexão do Raspberry(código base no Thonny) com o Ubidots, é possível observar um dashboard que é disponibilizado pelo próprio Ubidots onde é possível ver um gráfico representando as mudanças conforme as detecções do sensor de luminosidade(LDR)
