# 👷‍♀️🏭 Interface Homem-Máquina no AVR e Arduino
Este projeto consiste no desenvolvimento de um circuito com programação em AVR para uma interface de Homem-Máquina.

🛠 Tecnologias e Componentes Utilizados:

| Componente            | Modelo                                                                                                                               | Descrição                                                                                                                                     |
| :-------------------- | :----------------------------------------------------------------------------------------------------------------------------------- | :-------------------------------------------------------------------------------------------------------------------------------------------- |
| Microcontrolador      | [AVR - ATMega328P](https://ww1.microchip.com/downloads/en/DeviceDoc/Atmel-7810-Automotive-Microcontrollers-ATmega328P_Datasheet.pdf) | Plataforma Arduino Uno como interface                                                                                                         |
| IDE                   | [MPLabX](https://www.microchip.com/en-us/tools-resources/develop/mplab-x-ide)                                                        | Ambiente de Desenvolvimento Integrado - [Instalação](https://developerhelp.microchip.com/xwiki/bin/view/software-tools/ides/x/install-guide/) |
| Compilador            | [XC8](https://www.microchip.com/en-us/tools-resources/develop/mplab-xc-compilers/xc8)                                                | [Instalação](https://developerhelp.microchip.com/xwiki/bin/view/software-tools/xc8/install/)                                                  |
| Editor de código      | [Visual Studio Code](https://code.visualstudio.com/)                                                                                | [v1.97.2](https://code.visualstudio.com/sha/download?build=stable&os=win32-x64-user)                         |
| Construtor de projeto | [Makefile](https://stackoverflow.com/questions/32127524/how-to-install-and-use-make-in-windows)                                      | Power Shell<br>`winget install Chocolatey.Chocolatey`<br>`choco install make`                                                                 |
| Gravador do AVR       | [AVRDudess](https://github.com/ZakKemble/AVRDUDESS/releases/tag/v2.18)                                                               | [ZakKemble/AVRDUDESS/v2.18](https://github.com/ZakKemble/AVRDUDESS/releases/download/v2.18/AVRDUDESS-2.18-setup.exe)                          |
| Simulador eletrônico  | [SimulIDE](https://simulide.com/p/downloads/)                                                                                        | Power Shell<br>`winget install SimulIDE.SimulIDE`                                                                                             |
| Versionamento         | [git](https://git-scm.com/downloads)                                                                                                 | Power Shell<br>`winget install --id Git.Git -e --source winget`                                                                               |

Este projeto faz parte de uma atividade acadêmica e tem como objetivo a aplicação prática de conceitos de eletrônica e programação embarcada.

🗺️ Mapa de entradas e saídas:

Teclado:

| Função  | Dispositivo | Descrição | Pino (Arduino Uno) | Pino (ATmega328P) | PORT |
| :------ | :---------- | :-------- | :----------------- | :---------------- |:---- |
| Saída   | Teclado     | Linha 0   | O                  | 2                 | PD0  |
| Saída   | Teclado     | Linha 1   | 1                  | 3                 | PD1  |
| Saída   | Teclado     | Linha 2   | 2                  | 4                 | PD2  |
| Saída   | Teclado     | Linha 3   | 3                  | 5                 | PD3  |
| Entrada | Teclado     | Coluna 0  | 4                  | 6                 | PD4  |
| Entrada | Teclado     | Coluna 1  | 5                  | 11                | PD5  |
| Entrada | Teclado     | Coluna 2  | 6                  | 12                | PD6  |
| Entrada | Teclado     | Coluna 3  | 7                  | 13                | PD7  |


Display LCD (Interface):

| Função  | Dispositivo | Descrição | Pino (Arduino Uno) | Pino (ATmega328P) | PORT |
| :------ | :-----------| :-------- | :----------------- | :---------------- |:---- |
| Saída   | LCD         | D4        | 8                  | 14                | PB0  |
| Saída   | LCD         | D5        | 9                  | 15                | PB1  |
| Saída   | LCD         | D6        | 10                 | 16                | PB2  |
| Saída   | LCD         | D7        | 11                 | 17                | PB3  |
| Saída   | LCD         | RS        | 12                 | 18                | PB4  |
| Saída   | LCD         | EN        | 13                 | 19                | PB5  |

Botões e LED's:

| Função  | Dispositivo | Descrição | Pino (Arduino Uno) | Pino (ATmega328P) | PORT |
| :------ | :---------- | :-------- | :----------------- | :---------------- |:---- |
| Entrada | Botão       | Botão     | A0                 | 23                | PC0  |
| Entrada | Botão       | Botão     | A1                 | 24                | PC1  |
| Entrada | Botão       | Botão     | A2                 | 25                | PC2  |
| Saída   | LED         | Azul      | A3                 | 26                | PC3  |
| Saída   | LED         | Verde     | A4                 | 27                | PC4  |
| Saída   | LED         | Vermelho  | A5                 | 28                | PC5  |



| 🚦 Simulação no SimulIDE: |
|:----------------------------------------------------------------:|
| ![Semaforo-Temporizado](Semaforo-Temporizado.gif)                |
