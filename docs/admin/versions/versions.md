### Administrar Versões

Quando uma versão do projeto é selecionada, você verá detalhes específicos sobre a versão selecionada.

![Guia Idiomas da vista de versão](http://docs.zanata.org/en/release/images/version-view-languages.png)

1. Informações de projeto e versão
2. Informações gerais sobre o progresso da tradução da versão.
3. Uma lista de idiomas que estão disponíveis para tradução na versão.
4. Quando um idioma é selecionado, uma lista de documentos para a versão será mostrada, com informações de progresso para cada documento e o idioma selecionado.

As diferentes guias de uma versão oferecem mais informações sobre ela.

* __Documentos__ Semelhante à guia Idiomas, essa exibição permite selecionar um único documento para exibir informações detalhadas sobre o andamento de cada idioma.
* __Grupos__ Mostra se existem grupos aos quais a versão pertence.
* __Configurações__ (_Isso só está disponível para os Mantenedores do Projeto_) permite que o usuário altere as configurações da versão.

### Criando Versões
Os documentos de um projeto são agrupados em versões, em vez de serem adicionados diretamente ao projeto.

Para projetos simples, é típico criar uma única versão chamada 'master'. Outros projetos usam fluxos de trabalho nos quais há uma versão em desenvolvimento ativo e uma ou mais versões que estão sendo mantidas em um estado estável com apenas algumas pequenas alterações. Agrupar essas versões relacionadas sob o mesmo projeto permite uma reutilização mais fácil das traduções entre as versões.

1. [Crie um projeto.](./../../projects/projects/#criar-novos-projetos)
2. __Crie uma versão no projeto.__
3. Carregar documentos para a versão
4. Usando o site

### Criação de versão através do site
Para adicionar uma versão ao seu projeto, navegue até o projeto usando o menu ou painel do usuário, vá para a `Version` guia, clique em `More action` e selecione `New Version`. Se o seu projeto ainda não tiver versões, haverá um link no projeto no painel do usuário para ir direto para a criação da versão.

![img_btn_projeto](http://docs.zanata.org/en/release/images/version-create.png)
Botão de criação de versão em uma página inicial do projeto.
![img_link_cricao](http://docs.zanata.org/en/release/images/user-dashboard-create-version.png)

Link de criação de versão de atalho no painel do usuário.

A captura de tela a seguir mostra a página de criação da versão. As configurações nesta captura de tela criarão uma versão no projeto 'zanata-server' com ID 'master', que não requer uma fase de revisão para traduções e usará as localidades e validações do projeto. Veja abaixo os detalhes de cada opção.

![img_detalhes_version](http://docs.zanata.org/en/release/images/version-create-new.png)

#### ID da versão
Este é o identificador usado para se referir à versão no site da Zanata e ao usar um dos clientes da Zanata. Versões não usam um nome de exibição separado.

#### Tipo de projeto
Tipo de Projeto define o tipo de arquivos que seu projeto usa para armazenar sequências de origem e de tradução.

#### Copiar da versão anterior
Se selecionada, esta nova versão será baseada na versão selecionada. Veja [copiar versão](copiar_versao.md) para mais informações.

#### Revisão de traduções
A revisão de tradução é uma etapa opcional no processo de tradução em que um tradutor experiente pode verificar se as traduções são de qualidade suficiente.

Sem revisão de tradução, os tradutores salvam as traduções no estado 'traduzido', tornando-as imediatamente disponíveis para download e uso para o seu projeto.

Se estiver ativado, as traduções no estado 'traduzido' não serão consideradas prontas para download. Em vez disso, um revisor deve analisar as traduções e alterá-las para o estado "aprovado" ou "rejeitado". Somente as traduções no estado 'aprovado' são consideradas prontas para download.

A revisão de tradução acrescenta tempo e esforço extra ao processo de tradução, por isso não é recomendado para todos os projetos. A revisão da tradução pode ser ativada mais tarde, se necessário.

A desativação e a desativação da revisão não farão com que as traduções aprovadas percam seu status de aprovado. As traduções aprovadas permanecerão aprovadas, a menos que sejam substituídas por outra tradução. Quando a revisão é desativada, as traduções aprovadas serão tratadas da mesma forma que as traduções no estado "traduzido".

#### Configuração de versões

Depois que uma versão é criada, o mantenedor pode adicionar mais detalhes e comportamento de versão por meio da guia Configurações.

![Guia Configurações Gerais da Versão](http://docs.zanata.org/en/release/images/version-settings-button.png)

##### Configurações Gerais
![Guia Configurações Gerais da Versão](http://docs.zanata.org/en/release/images/admin-version-settings.png)

##### Tipo de projeto
As configurações de tipo de projeto, por padrão, herdam das configurações do projeto, mas os mantenedores podem selecionar um tipo de projeto diferente para a versão.

##### Tornar esta versão somente leitura
Este botão é usado para definir uma versão para somente leitura, o que impede que as traduções sejam inseridas. Isso pode ser útil em alguns casos, mas deve ser usado com moderação para que os tradutores possam trabalhar em seu projeto.

Isso pode ser alternado usando o mesmo botão, conforme desejado.

##### Excluir esta versão
Este botão é usado para excluir esta versão e removê-la da lista de projetos públicos. Esta ação não pode ser desfeita, portanto, use com cautela.

#### Configurações de documentos
![Guia Configurações dos Documentos da Versão](http://docs.zanata.org/en/release/images/version-documents-settings.png) 

##### Adicionando documento de origem
Clique em `+` assinar no canto superior esquerdo, na guia Documentos, em Configurações. Navegue ou arraste seus documentos para a caixa de diálogo e clique em `Upload Documents`.

#### Configurações de Idiomas
![Guia Configurações de idiomas da versão](http://docs.zanata.org/en/release/images/version-languages-settings.png)

##### Localidades personalizadas
Por padrão, seu projeto estará disponível para tradução para um conjunto de locales definidos para o seu projeto ou no servidor Jtech Zanata se o projeto não tiver localidades personalizadas. Se a sua versão exigir um conjunto diferente de localidades do seu projeto, clique `Enable` ou `Disable` no lado direito da localidade.

##### Lista personalizada de validações
Se a sua versão exigir um conjunto diferente de validações que o projeto pai, elas podem ser selecionadas aqui. Se as validações personalizadas não forem especificadas, as validações especificadas para o seu projeto serão usadas. Uma vantagem de herdar validações do projeto é que novas validações podem ser adicionadas ao projeto sem precisar adicioná-las a cada versão diferente.
