Universidade Federal do Rio Grande do Norte - Departamento de Engenharia de Computação e Automação - DCA
Time Poti de Futebol de Robôs
=================
> Para utilização do sistema do Time Poti é necessário a utilização de um sistema operacional Linux. 

> A manipulação do sistema é feita via Terminal do Linux, tendo a interface gráfica apenas o módulo de calibração.

Getting Started
---------------

### Instalação de bibliotecas e pacotes

Inicialmente, é interessante que seu sistemas esteja atualizado. Para isso, deve ser utilizado o comando:

```
  sudo apt-get update
```

Comando para instalação de pacotes para utilização do bluetooth
```
sudo apt-get install bluetooth bluez-utils blueman
```

Após esse comado, verificar se na pasta include do computador está a pasta `/usr/include/bluetooth`. Caso não, use o comando abaixo:
```
sudo apt-get install build-essential libbluetooth-dev libdbus-1-dev
```

### Make Make Make Make Make...
Agora, utilizar os comandos a seguir em todas as pastas da pasta `libsrc`:
```
make
make clean
make install
```

Ir nas pastas `program/calibrador` e `program/main` e utilizar os comandos:
```
make clean
make 
```

Após essas etapas, você pode fazer a `calibração` do campo com seus objetos ou fazer um jogo. 
Caso opte em calibração, deve-se verificar se a câmera a ser usada está referenciada corretamente no código do sistema. Caso não, ir em `libsrc/camera/camera.cpp` e substituir na linha 
```C++
name= "/dev/video1";  
```
o 1 pela referência adequada: 0, 1, 2... 

### Calibração e Jogo

Para fazer a calibração, basta executar em `program/calibrador`
```
./calibrador
```

Ou 

Para fazer um jogo, basta executar em `program/main`
```
./main
```

> Divirta-se!!
