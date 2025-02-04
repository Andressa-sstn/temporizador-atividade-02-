# temporizador-atividade-02-

# Temporizador de Disparo de LEDs (One Shot) - Raspberry Pi Pico

## Descrição do Projeto

Este projeto controla 3 LEDs (azul, vermelho e verde) conectados ao **Raspberry Pi Pico** e utiliza um **botão (pushbutton)** para ativar os LEDs. Quando o botão é pressionado, os LEDs são acesos, e após um determinado tempo (através de temporizadores), os LEDs desligam de forma progressiva (um de cada vez).

### Funcionalidade

1. **Quando o botão é pressionado**:
   - Todos os 3 LEDs são acesos ao mesmo tempo.
   
2. **Com o tempo**:
   - Após 1 segundo, o LED azul é desligado.
   - Depois de mais 1 segundo, o LED vermelho é desligado.
   - Finalmente, após mais 1 segundo, o LED verde é desligado.
   
Essa sequência simula um **temporizador de disparo (One Shot)**, onde os LEDs são desligados em intervalos progressivos.

### Componentes Utilizados

- **1x Raspberry Pi Pico** (ou **Pico W**)
- **3x LEDs** (Azul, Vermelho e Verde)
- **3x Resistores de 330Ω**
- **1x Pushbutton**
- **Fios de conexão**

### Esquema de Conexões

- O **LED Azul** está conectado no **pino GP15**.
- O **LED Vermelho** está conectado no **pino GP16**.
- O **LED Verde** está conectado no **pino GP17**.
- O **Pushbutton** está conectado no **pino GP14**, com um resistor de pull-down.

### Como Usar

1. **Instalar o Ambiente de Desenvolvimento**:
   - Certifique-se de ter o **VS Code** instalado.
   - Instale o **Pico SDK**

2. **Compilar e Rodar o Código**:
   - Abra o projeto no **VS Code**.
   - Compile o código usando o comando 
   .

3. **Carregar o Código no Raspberry Pi Pico**:
   - Pressione e segure o botão **BOOTSEL** no seu Raspberry Pi Pico e conecte-o ao computador via USB.
   - O dispositivo será montado como uma unidade de armazenamento.
   - Arraste e solte o arquivo `.uf2` na unidade de armazenamento montada.

4. **Testar o Comportamento**:
   - Quando o Raspberry Pi Pico for reiniciado, pressione o **botão** para iniciar o ciclo dos LEDs.
   - Observe que os LEDs serão acesos e apagados em sequência após o tempo programado.

### Código-fonte

O código está localizado no arquivo `main.c` e utiliza a funcionalidade de interrupção do botão para iniciar a sequência de temporizador e controle dos LEDs.


  
