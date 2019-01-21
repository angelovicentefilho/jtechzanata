## Mesclar traduções de outra versão do projeto
As traduções de mesclagem permitem que os mantenedores do projeto copiem as traduções em diferentes versões do projeto com base no contexto correspondente. (Veja abaixo as regras de correspondência de contexto)

## Restrições
* Este recurso está disponível apenas para os mantenedores do projeto.
* Somente as traduções que estão no estado traduzido / aprovado serão usadas.
* A conversão de mesclagem só pode ser executada se não houver outras operações de cópia em andamento para a versão selecionada, como copy-trans ou copy version.

## Regra da qual as traduções serão copiadas

|   De                                  |Para                  |    Cópiar?               |
|---------------------------------------|----------------------|-------------------------:|
| fuzzy/untranslated                    | any                  |    Não                   |
| different source text/document id     | any                  |    Não                   |
| resId/msgctxt/locale          	    | any                  |    Não                   |
| traduzido / aprovado                  | untranslated/fuzzy   |    Sim                   |
| traduzido / aprovado                  | traduzido/aprovado   | Copiar se mais recente   |


## Fazer merge de traduções
1. Entrar no Jtech Translate Zanata.
2. Selecione uma versão do projeto para a qual você deseja copiar traduções.
3. Expanda o menu `More Action` no canto superior direito e clique em `Merge Translations`. Esta ação só está disponível se você for um mantenedor do projeto.
![Mais menu de ação na página de versão do projeto](http://docs.zanata.org/en/release/images/version-more-action-menu.png)
4. Na caixa de diálogo exibida, selecione a versão do projeto da qual você deseja copiar as traduções.
![Caixa de diálogo de conversão de mesclagem](http://docs.zanata.org/en/release/images/version-merge-trans-dialog.png)
5. Se você não deseja substituir traduções traduzidas / aprovadas, verifique se `Keep existing translated/approved translations` está marcado. Se esta opção não estiver marcada, as traduções traduzidas / aprovadas serão substituídas por traduções traduzidas / aprovadas mais recentes, se estiverem disponíveis.
6. Clique no botão `Merge Translations` para iniciar o processo.
7. O progresso do processo de mesclagem é mostrado por uma barra de progresso na página de versão.
![Mesclar tradução em andamento](http://docs.zanata.org/en/release/images/version-merge-trans-progress.png)

## Cancelar tradução de mesclagem
__Nota__: _Isso só impedirá que mais traduções sejam mescladas. Todas as traduções que já foram mescladas permanecerão mescladas_.

1. Vá para a seção da barra de progresso na página de versão do projeto.
2. Clique no botão `Cancel`no painel superior direito.
![Cancelar tradução de mesclagem em andamento](http://docs.zanata.org/en/release/images/version-merge-trans-cancel.png)