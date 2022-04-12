# Instalação do Quartus em Linux

<!--- Texto --->

## Download

Download [neste link](https://download.altera.com/akdlm/software/acdsinst/13.1/162/ib_tar/Quartus-web-13.1.0.162-linux.tar).

## Download de Bibliotecas 32 Bits

<!--- Texto --->

### Bibliotecas para rodar o Setup:

    $ sudo dpkg --add-architecture i386
    $ sudo apt update
    $ sudo apt-get install libstdc++5:i386 libmotif4:i386 libxp6:i386 libcurl4:i386

### Biblioteca para rodar o Quartus II 13.1:

    $ sudo add-apt-repository ppa:linuxuprising/libpng12
    $ sudo apt update
    $ sudo apt install libpng12-0

## Instalação do Quartus

No local do download extraia os arquivos compactados em .tar e execute

    $ ./setup.sh

O processo de instalação deve ocorrer normalmente.

## Rodando o Quartus

<!--- Texto --->

    $ <install_path>/quartus/bin/quartus --64bit

## Configurações Adicionais

Ao utilizar o Quartus II foi possível criar um projeto e compilar códigos em VHDL. Porém durante o uso de simulações com o University Program VWF ocorreu um erro:

    "ModelSim executable not found"

Para resolver esse problema vá em:

    Tools &#8594; Options &#8594; EDA Tool Options

Apenas um local estará com link. E é o local errado!
Recorte e cole o link no campo **ModelSim**.
