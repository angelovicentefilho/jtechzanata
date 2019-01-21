As distros utilizadas para instalação do Zanata Client são:

* [Fedora](#fedora)
* [Outros](#outros)

## Fedora

Existem duas maneiras de instalar o zanata-client, via `0install` ou `dnf`.

### Com 0install

**Nota: Se você já tiver instalado o `zanata-cli` Ivy ou o yum, será necessário desinstalá-lo primeiro**

1. Se você não instalou o `0install`, execute os seguintes comandos para instalar com dependências:
    
    !!! Tip "Instalação do 0install"
        ```python
            sudo yum -y install 0install java-1.8.0-openjdk unzip
        ```


1. Para instalar o zanata-cli, execute:
    
    !!! Tip "Instalação do Zanata Client"
        ```Bash
            mkdir -p ~/bin
            0install destroy zanata-cli
            0install -c add zanata-cli https://raw.githubusercontent.com/zanata/zanata.github.io/master/files/0install/zanata-cli.xml
            0install -c update zanata-cli
        ```

1. Execute `zanata-cli --help` para o verificar os comandos.
2. Para atualizar o zanata-cli, execute:

    !!! Tip "Atualização do Zanata Client"
        ```
         0install -c update zanata-cli
        ```

### Com dnf

O pacote que contém `zanata-cli`, já está no repositório oficial do Fedora.

**Nota: Se você instalou anteriormente `zanata-cli` com o Ivy ou 0install, será necessário desinstalá-lo primeiro**

1. Para instalar zanata-cli, execute:

    !!! Tip "Instalando o Zanata Client"
        ```
         sudo dnf -y install zanata-client
        ```

1. Execute `zanata-cli --help` para verificar os comandos.

1. Para atualizar o zanata-cli, execute:

    !!! Tip "Atualização do Zanata Client"
        ```
            sudo dnf -y update zanata-client
        ```

## Outros

**Nota: Se você instalou `zanata-client` anteriormente por meio de outro método, será necessário desinstalá-lo para que isso funcione.**

1. Siga 0Install em [0Install para Linux](http://0install.net/install-linux.html/).
2. Instale o Java JRE (1.8 em diante)
3. Para instalar o zanata-cli, execute:

    !!! Tip "Instalação do Zanata Client"
        ```Bash
            mkdir -p ~/bin
            0install destroy zanata-cli
            0install -c add zanata-cli https://raw.githubusercontent.com/zanata/zanata.github.io/master/files/0install/zanata-cli.xml
            0install -c update zanata-cli
        ```

4. Execute `zanata-cli --help` para verificar os comandos.

5. Para atualizar o zanata-cli, execute:

    !!! Tip "Atualização do Zanata Client"
        ```Bash
            0install -c update zanata-cli
        ```

    

## Comandos úteis 0install
* Executar Zanata-CLI sem alias

    !!! Tip "Executando o comando"
        ```
            0launch https://raw.githubusercontent.com/zanata/zanata.github.io/master/files/0install/zanata-cli.xml {command}
        ```