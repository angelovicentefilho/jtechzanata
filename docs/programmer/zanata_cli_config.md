O zanata-cli requer Configuração do Usuário e Configuração da Versão do Projeto.

## Configuração do usuário
A configuração do usuário armazena suas credenciais para que o zanata-cli possa provar ao servidor que as solicitações são de você, e não de um impostor. As informações na sua configuração de usuário devem ser mantidas em segredo.

O zanata-cli espera encontrar a configuração do usuário .config/zanata.ini dentro do seu diretório de usuários.

Para adicionar configuração para um servidor Jtech Zanata:

1. Use o seu editor de texto favorito para criar ou abrir `zanata.ini` no `~/.config/.`
1. Entre no servidor Jtech Zanata e navegue até a página de configurações do usuário
1. Assegure-se de que uma chave de API seja mostrada. Se você não tiver uma chave de API, clique em "Gerar chave de API" agora.
´![Página de configurações do usuário](http://docs.zanata.org/en/release/images/302-user-settings.png)
1. Copie o conteúdo da caixa de texto denominada 'Configuração [zanata.ini]'.

1. Cole as linhas copiadas `zanata.ini` e salve o arquivo.

## Configuração da versão do projeto
A configuração do projeto armazena informações sobre uma versão do projeto e deve ser mantida no diretório do projeto.

O zanata-cli espera encontrar a configuração da versão do projeto em um arquivo chamado `zanata.xml` no diretório do projeto.

Para adicionar a configuração da versão do projeto ao diretório do seu projeto:

1. Entre no servidor Jtech Zanata e navegue até a versão apropriada do seu projeto.
1. Clique no link `Download config file` para iniciar o download de `zanata.xml`. 
![Baixar link do arquivo de configuração na página da versão](http://docs.zanata.org/en/release/images/350-version-config-file.png)
1. Salve `zanata.xml` no diretório do seu projeto.

Essas etapas devem ser repetidas para cada versão do projeto antes de usar qualquer comando zanata-cli para a versão do projeto.

Você pode personalizar `zanata.xml` com ganchos de comando para que outras ferramentas sejam executadas automaticamente antes ou depois dos comandos do Jtech Zanata.