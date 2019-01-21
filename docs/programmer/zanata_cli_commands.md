Para inicializar um projeto a partir da linha de comando, o comando `init` pode ser usado. Este comando irá guiá-lo através dos passos necessários para configurar um projeto novo ou existente e começar a usar o Jtech Zanata.

## Começando
### init
A primeira coisa a fazer é digitar o seguinte comando no console: `zanata-cli init`

O cliente irá perguntar qual dos seus servidores Jtech Zanata preferidos ele precisa usar para registrar seu novo projeto (esta informação é retirada do seu `zanata.ini` arquivo; se o servidor desejado não aparecer na lista, ele deve ser adicionado a este arquivo).

 ```
    [INFO] Loading project config from zanata.xml
    [INFO] Loading user config from /home/camunoz/.config/zanata.ini
        Found servers in zanata.ini:
        1)    http://localhost:8080/zanata/
        2)    https://translate.jboss.org/
        3)    https://translate.zanata.org/zanata/
    [?] Which Jtech Zanata server do you want to use?
 ```

Selecione o servidor Jtech Zanata para usar digitando o número e pressionando ENTER. O cliente perguntará agora se você deseja criar um novo projeto ou usar um existente da sua instância:

    ```
        [?] Do you want to 1) select an existing project or 2) create a new one (1/2)?
    ```
De acordo com a sua seleção, o cliente solicitará informações sobre o seu novo projeto e continuará a criá-lo, ou ele terá a opção de selecionar um existente do servidor.

```
    [?] What project ID/slug do you want to have (must start and end with a letter 
    or number, and contain only letters, numbers, underscores and hyphens):
    $ my-project-id
    [?] What project name do you want to have:
    $ My Project Name
    [?] What is your project type ([utf8properties, properties, gettext, podir, 
    xliff, xml, file])?
    $ podir
    [>] Project created. Now it's time to create a version to host your files.

    [?] What version ID/slug do you want to have:
    $ master
    [>] Version created.
```

O cliente Jtech Zanata continuará a fazer perguntas e fornecer informações sobre os próximos passos necessários para você começar a trabalhar no seu projeto na Jtech Zanata.
### push
Para carregar documentos para sua versão de projeto, o comando `push` pode ser usado.

#### Upload de Documento de Origem
O comando básico para o upload de documentos é `zanata-cli push`. O comando `push` deve sempre ser executado a partir do diretório que contém `zanata.xml`.

O comando de envio mais simples é:

`zanata-cli push`

Este comando irá:

1. Procurar por documentos de origem em um diretório especificado como `src-dir` e qualquer um de seus subdiretórios (src-dir pode ser especificado em zanata.xml ou na opção de linha de comando. O padrão é o diretório atual).
2. Exibir as configurações atuais e lista de documentos de origem que foram encontrados.
3. Confirmar que você deseja continuar com o upload.
4. Fazer upload dos documentos de origem localizados para o servidor.

_Nota:_ Se os arquivos de origem estiverem no mesmo diretório que os arquivos não originais que possuem a mesma extensão, como ao usar arquivos Java `.properties` para conversão e configuração, a opção `--includes` ou `--excludes` deve ser usada para informar ao Jtech Zanata quais arquivos devem ser enviados.

Para obter uma lista completa das opções disponíveis para push, execute `zanata-cli help push`

#### Upload do documento de tradução
O comando push também pode fazer upload de traduções. Isto é principalmente para uso quando a tradução começou em seu projeto antes de se mudar para a Jtech Zanata. Os tradutores também podem usar este comando para fazer upload de traduções, embora a tradução no site da Jtech Zanata seja mais segura.

Para enviar traduções em vez de documentos de origem, adicione a opção `--push-type trans`:

```Bash
    zanata-cli push --push-type trans --trans-dir trans
```

Para dar push nos documentos de origem e de tradução juntos, use `--push-type both`.

Esses comandos farão upload de todas as traduções disponíveis para as localidades especificadas em `zanata.xml`, a menos que a opção `-l` ou `--locales` seja usada para especificar um conjunto menor de localidades. Por exemplo: `-l ja,de`.

_Nota_: Os documentos de tradução devem ser nomeados adequadamente para corresponder a um documento de origem. O nome apropriado depende do seu tipo de projeto. Por exemplo, se o comando acima for usado para um projeto Java Properties com um documento de origem `src/strings/messages.properties`, uma tradução em japonês para o documento será em `src/strings/messages_ja.properties`.

```Bash
    src
    strings
        messages.properties
        messages_ja.properties
```  

Se você não tiver certeza sobre o layout e a nomenclatura dos arquivos de tradução no tipo de projeto selecionado, poderá fazer um teste de avaliação e examinar a saída. Isso pode ser feito copiando `zanata.xml` para uma pasta vazia e executando um comando `pull` como:

```Bash
    zanata-cli pull --src-dir src/strings --trans-dir src/strings --create-skeletons
```
A opção `--create-skeletons` é usada para garantir que os arquivos serão gravados mesmo se não houver traduções.
### pull
Para baixar documentos de sua versão de projeto, o comando `pull` pode ser usado.

Estas instruções assumem que você instalou o Zanata-CLI conforme mostrado em Instalando o cliente e salvou a configuração do usuário e do projeto conforme mostrado em Configurando o cliente .

#### Download do Documento de Tradução
O comando básico para baixar documentos é `zanata-cli pull`. O comando `pull` sempre deve ser executado a partir do diretório que contém `zanata.xml`.

O comando de pull mais simples é:

```Bash 
    zanata-cli pull
```
Este comando irá:

1. Procurar as localidades da versão do projeto para extrair do servidor (a menos que seja especificado em zanata.xml ou na opção da linha de comandos).
2. Exibir as configurações atuais e a lista de localidades que serão baixadas.
3. Confirmar que você deseja prosseguir com o download.
4. Baixar as versões traduzidas de quaisquer documentos que possuam traduções.

Os documentos sem tradução não serão baixados, a menos que especificamente solicitado, adicionando a opção `--create-skeletons`.

Para baixar apenas alguns locales, use a opção `-l` ou `--locales`. Por exemplo, para baixar apenas traduções em japonês e russo, posso executar `zanata-cli pull -s src -t trans -l ja,ru`. Você também pode modificar as localidades `zanata.xml`.

Para obter uma lista completa das opções disponíveis para `pull`, execute `zanata-cli help pull`

#### Download do Documento de Origem
O comando `pull` também pode baixar documentos de origem. Geralmente, isso é apenas para fins de referência, pois os documentos de origem não podem ser alterados no servidor.

Para obter traduções em vez de documentos de origem, adicione a opção da seguinte `--pull-type source`:

```Bash
    zanata-cli pull --pull-type source --src-dir src/strings
```

Para reunir documentos de origem e de tradução, use `--pull-type both`.