## Administrar Projetos

Para administrar um projeto o _Administrador_ pode criar, ler e gerenciar os times.

### Visualizar Projeto

Quando um projeto é selecionado, você será levado a uma visão geral do projeto. Isto mostrará uma lista das versões disponíveis, bem como uma indicação do progresso da tradução.

![img01](http://docs.zanata.org/en/release/images/project-view-versions.png)

Visão do Projeto

1. Informações do Projeto
2. Alterna entre as diferentes visualizações disponíveis para o projeto
3. Diferentes opções para classificar as versões do projeto.

As diferentes visões de um projeto oferecem mais informações sobre ele.

1. Versões mostra todas as versões do projeto
2. As pessoas mostram os Mantenedores, Tradutores e Revisores do projeto.
3. O glossário mostra entradas do glossário para o projeto.
4. Sobre mostra mais informações sobre o projeto.
5. Configurações (Isso só está disponível para os Mantenedores do Projeto) permite que o usuário altere as configurações do projeto.

### Criar novos projetos

Qualquer pessoa com uma conta pode fazer upload de strings de origem para a Jtech Translate Zanata. O primeiro passo é criar um projeto:

1. **Crie um projeto**.
2. Crie uma versão no projeto.
3. Carregar documentos para a versão:
4. Usando o site
5. Usando o comando push do cliente da linha de comandos

#### Criação de projetos através do site

Para começar a criar um projeto no site, clique no botão `+` na guia `Project` do seu Dashboard.

![img02](http://docs.zanata.org/en/release/images/create-project.png)

A proxima tela mostra um exemplo de criação de um projeto. Os campos cadastrados foram preenchidos para ilustrar o processo. Este exemplo criaria um projeto com a URL terminando em __/zanata-server__, que será exibido na lista de projetos do servidor.

![img03](http://docs.zanata.org/en/release/images/create-project-completed.png)

Vamos ver o que significa cada campo.

### ID do projeto
O ID do projeto é um identificador exclusivo do seu projeto que será usado na URL do projeto e nos arquivos de configuração do cliente. Aceita apenas letras, números pontos, hifens e sublinhados e não pode conter espaços.

### Nome
Nome é o nome de exibição do seu projeto. O nome é mostrado em todos os locais em que seu projeto é exibido, como a lista de projetos, o painel do usuário e a página do projeto. Este deve ser um nome que permita que os tradutores reconheçam facilmente seu projeto.

### Descrição
Uma breve descrição para fornecer um pouco mais de informações para os tradutores identificarem seu projeto. Descrição é exibida na lista de projetos.

### Tipo de projeto
Tipo de Projeto define o tipo de arquivos que seu projeto usa para armazenar sequências (chaves) de origem e de tradução. Essa configuração garante que os arquivos do seu projeto sejam baixados no formato correto.

Há uma breve descrição para cada tipo de projeto ao lado de cada opção de tipo de projeto. Se a descrição for insuficiente, mais informações sobre cada tipo de projeto estarão disponíveis nos [Tipos de Projeto](#tipos-de-projetos-suportado) .

### Gerenciamento do projetos
Depois que um projeto é criado, o mantenedor pode adicionar mais detalhes e comportamento do projeto por meio da guia Configurações.

![img08](http://docs.zanata.org/en/release/images/project-settings-button.png)

### Configurações Gerais
![img_1_](http://docs.zanata.org/en/release/images/admin-project-settings.png)
Guia Configurações gerais do projeto

### Excluir este projeto
Este botão é usado para excluir um projeto e removê-lo da lista de projetos públicos. Você não poderá mais acessá-lo. Esta ação não pode ser desfeita, portanto, use com cautela.

### Removendo uma linguagem de projeto
Para remover um idioma da lista de localidades disponíveis, primeiro mova o cursor sobre o idioma e, em seguida, clique no "X" exibido.

![img_2_](http://docs.zanata.org/en/release/images/project-languages-remove.png)

### Configurações de permissões

![img_3_](http://docs.zanata.org/en/release/images/project-permissions-settings.png)

Nota: Os mantenedores também podem ser adicionados e removidos através da equipe do projeto .

### Tipos de projetos suportado

#### Qual tipo de projeto?
Tipos de arquivos são suportados (seletivamente) através do Framework Okapi.

#### Tipos Suportados
##### Não especificado
Essa seleção de tipo de projeto é mostrada apenas para projetos antigos que foram criados antes de os tipos de projetos serem mostrados no servidor. Se o seu projeto ou versão do projeto tiver esse tipo, você deve alterá-lo para o tipo apropriado. Quando o tipo de projeto não for especificado, você não poderá fazer upload de arquivos de origem pela interface da Web e terá que adicionar manualmente um tipo de projeto ao arquivo de configuração do cliente.

#### Arquivo
Veja o [formato suportado](supported_formats.md).

Anteriormente, o Raw, File é um tipo de projeto __experimental__ que fornece suporte limitado para arquivos de texto simples, LibreOffice, HTML, inDesign e DTD. Os arquivos de origem devem estar em um diretório separado dos arquivos de tradução. O comportamento deste tipo de projeto está sujeito a alterações sem aviso prévio enquanto estiver em estado experimental.

O analisador reconhece novas linhas para `.txt` e parágrafos para `.html`.

#### Gettext `.pot`
Usa o formato gettext com um único arquivo de modelo (.pot). Arquivos de tradução (.po) são nomeados com o identificador de localidade.

#### Podir `.pot`
Usa o formato gettext com vários arquivos de modelo (.pot). Os arquivos de tradução usam o mesmo nome dos arquivos de modelo, mas são colocados em um diretório nomeado com o identificador de localidade. Use este tipo para projetos de public/docbook.

#### Propriedades `.properties`
Lida com arquivos de propriedades normais do java usando a codificação ISO-8859-1 (Latin-1). Os arquivos de propriedades Java requerem que caracteres não latinos-1 sejam escapados com caracteres de escape unicode (por exemplo, \ uFEDC). 
Nota: Atualmente, os arquivos de propriedades só podem ser carregados usando o __Zanata CLI Client__ ou __Gerador Auxiliar__

#### Utf8Properties `.properties`
Manipula arquivos de propriedades Java não padrão que usam codificação UTF-8 e não usam caracteres de escape unicode. 
Nota: Atualmente, os arquivos de propriedades só podem ser carregados usando o __Zanata CLI Client__ ou __Gerador Auxiliar__

### Suporte parcial/limitado
#### Xliff
Não é ativamente suportado. (Detalhes sobre o esquema de arquivos esperamos que em breve ...)

#### Xml
Não é ativamente suportado. (Detalhes sobre o esquema de arquivos esperamos que em breve ...)