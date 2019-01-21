![Visualização do editor](http://docs.zanata.org/en/release/images/editor-overview.png)

## Partes

### 1. Breadcrumbs
Links para Projeto -> Versão -> Visualização de documentos -> Nome do documento. Cada link redirecionará para a respectiva página.

### 2. Estatística
Estatísticas e horas restantes do atual documento de tradução do documento.

### 3. Visualizações
Veja [visualizações]() para mais informações.

### 4. Pesquisar e filtrar
Permitir que os tradutores pesquisem texto e filtrem por status de tradução. As traduções podem estar em um dos vários estados que indicam onde estão no fluxo de trabalho de tradução. Os estados são:

Vazio: nenhuma tradução foi inserida. **Fuzzy**: uma tradução foi inserida, mas não é considerada pronta para uso. **Translated**: uma tradução foi inserida e o tradutor a considera pronta para uso. e somente em projetos com revisão ativada:

**Approved**: uma tradução foi inserida e um revisor a considera pronta para uso. **Reject**: uma tradução foi inserida, mas um revisor não a considera pronta para uso. Você pode mostrar ou ocultar traduções com qualquer um desses estados usando as configurações de filtro acima da tabela do editor. Apenas marque a categoria '**Incomplete**' ou '**Complete**', ou verifique os estados individuais dentro de cada categoria para mostrar traduções de interesse (por exemplo, mostrando apenas traduções Rejeitadas para alterá-las após a revisão).

Além de filtrar por estados, você pode marcar a caixa de seleção "**Invalid**" para mostrar apenas traduções que correspondam a um dos estados selecionados e tenham um ou mais avisos de validação.

### 5. Cadeia de Origem
Strings mostram o texto original para o qual uma tradução é necessária. O texto em si é exibido em uma caixa de texto e não pode ser alterado. Além do texto de origem, algumas outras informações úteis são mostradas.

Os números de linha são mostrados à esquerda das caixas de texto de origem e de tradução. Linhas longas serão exibidas em várias linhas na caixa de texto, mas terão apenas um número de linha.

Os caracteres em branco são mostrados na fonte e no texto da tradução para permitir uma tradução precisa. Os espaços são exibidos com um sublinhado cinza fraco, novas linhas são mostradas com um caractere de pilotar cinza fraco (¶) e as guias são mostradas com um caractere cinza-seta-para-barra (⇥).

O número da string no documento é mostrado abaixo da string de origem da linha atualmente selecionada, junto com o comentário de origem, se houver. Clicar no número da string faz com que algumas informações extras sobre a string sejam exibidas.

À esquerda do número da string, há um ícone de favoritos. Clicar no ícone do marcador atualiza o URL para que você possa criar um link diretamente para essa sequência específica.

### 6. Validação de tradução
Conforme você digita, as validações serão executadas no texto digitado. Se alguma validação falhar, os avisos serão exibidos aqui. Avisos são apagados quando o texto não falha mais na validação.

### 7. Ações de Tradução
Da esquerda para a direita: Salvar como traduzido, Salvar como Fuzzy, Cancelar alterações, Histórico de tradução, desfazer a tradução.

### 8. Configurações do editor
De cima para baixo: Notificação, sala de bate-papo, configurações, opções de validação.

### 9. Paginação
Navegação de página do documento.

### 10. Memória de tradução
A Translation Memory (TM) procura traduções de strings iguais ou semelhantes à string de origem selecionada atualmente. A pesquisa examina todos os projetos no Zanata para as sequências mais semelhantes que têm uma tradução traduzida ou aprovada no idioma correto.

As correspondências podem ser copiadas para a caixa de texto de tradução e usadas como estão ou modificadas antes de salvar. Para copiar TM corresponde à caixa de texto selecionado, clique no `Copy` botão ao lado do jogo, ou usar `Ctrl+Alt+1` a `Ctrl+Alt+4` atalhos de teclado para copiar o primeiro a quarto jogo na lista.

Você também pode pesquisar a TM por outras frases digitando-as na caixa de texto TM e clicando em `Search`.

### 11. Glossário
Se um glossário tiver sido enviado para o seu idioma, cada palavra na linha atualmente selecionada será pesquisada para uma entrada do glossário.

## Editor somente leitura
Se você não fizer parte dessa equipe de idiomas, o editor será aberto como modo somente leitura. Você estará restrito a somente visualizar a fonte e as traduções no editor.

![Editor somente leitura](http://docs.zanata.org/en/release/images/editor-readonly-indicator.png)

## Definições

![Configurações do editor](http://docs.zanata.org/en/release/images/editor-settings.png)

* **Botões do editor** - Mostrar/ocultar botões do editor.
* **Inserir chave salva imediatamente** - Salvar tradução quando a `Enter` tecla de acesso do usuário .
* **Usar realce de sintaxe Editor** - Ative o realce de sintaxe no editor. (Atenção: sem verificação ortográfica, as linhas longas podem ter alguns problemas de quebra automática)
* **Mostrar aviso `Save as Approved`** - Mostrar aviso quando Salvar como Aprovado é acionado por meio do atalho do teclado
* **Tamanho da página** - Permite que o usuário personalize documentos para mostrar por página.
* **Mostrar sugestão de tradução** - Mostrar/ocultar painel de memória de tradução
* **Mostrar Sugestão Glossária** - Mostrar/ocultar o painel do glossário
* **Layout** - Personalize a exibição de lista documento com `Compact`, `Default` e `Loose`.
* **Mostrar erros do sistema** - Mostra mensagens detalhadas em novas janelas quando ocorrem erros.

## Validações
![Configurações de validação do editor](http://docs.zanata.org/en/release/images/editor-validations.png)

Os tradutores podem ativar ou desativar a verificação de validação em suas traduções, exceto aquelas que são aplicadas pelos mantenedores do projeto.

## Atalhos

### Global

|Atalho  |   Ação|
|--------|-------|
|`Alt+Y`   |   Mostrar todos os atalhos de teclado disponíveis|
|`Esc`|   Fechar lista de atalhos de teclado|
|`Alt+X`|Ativar modo de atenção|
|`Alt+L`|Mostrar lista de documentos|
|`Alt+O`|Mostrar visualização do editor|
|`Alt+P`|Mostrar pesquisa ampla do projeto e substituir|

### Editor

|Atalho|Açao|
|------|----|
|`Alt+PageUp`|Mover para o anterior Fuzzy / Rejected / Untranslated|
|`Alt+PageDown`|	Mover para o próximo Fuzzy / Rejected / Untranslated|
|`Alt+Up` e `Alt+J`|	Mover para a linha anterior|
|`Alt+Down` e `Alt+K`|	Mover para a próxima linha|
|`Alt+G` e `Alt+X,G`|	Copiar texto da string de origem|
|`Ctrl+Enter`|	Salvar como traduzido|
|`Ctrl+S`|	Salvar como Fuzzy|
|`Ctrl+Alt+1` e `Ctrl+Alt+Num 1`|	Copiar do resultado da correspondência de memória de tradução no.1|
|`Ctrl+Alt+2` e `Ctrl+Alt+Num 2`|	Copiar do resultado da correspondência de memória de tradução no.2|
|`Ctrl+Alt+3` e `Ctrl+Alt+Num 3`|	Copiar do resultado da correspondência de memória de tradução no.3|
|`Ctrl+Alt+4` e `Ctrl+Alt+Num 4`|	Copiar do resultado da correspondência de memória de tradução no.4|
|`Ctrl+Alt+H` e `Alt+X,H`|	Ativar ou desativar o destaque da sintaxe. A verificação ortográfica não funcionará quando |