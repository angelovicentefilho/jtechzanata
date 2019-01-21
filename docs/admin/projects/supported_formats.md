Um novo recurso experimental foi adicionado para permitir o upload e o download de tipos adicionais de documentos.

Esse recurso fornece a capacidade de fazer upload e download de documentos usando o site, a interface REST ou o cliente Zanata.

### Formatos Suportados
Formatos suportados incluem:

* Plain-text (.txt)
* Web (.html, .htm)
* Subtitles (.srt, .vtt, .sub, .sbv)
* Qt Linguist (.ts)
* Document Type Definition (.dtd)
* XLIFF (.xlf) - limited support
    * Open Document Format (LibreOffice):
    * Open Document Text (.odt)
    * Open Document Presentation (.odp)
    * Open Document Spreadsheet (.ods)
    * Open Document Graphics (.odg)
* InDesign Markup Language (.idml)
* JSON (.json)

Open Document Formula (.odf) e o Open Document Database (.odb) não são suportados. Os formatos de localização dedicados do JSON (por exemplo, i18next) não são suportados. Os arquivos JSON serão tratados como documentos brutos e strings independentes (por exemplo, valores de matriz) serão incluídos na análise.

### Problemas conhecidos
Esse é um recurso experimental e existem vários problemas que devem ser considerados ao usar esse recurso:

### Tradução Offline no Formato do Documento Original Apenas Parcialmente Suportado
A tradução off-line no formato do documento original deve ter exatamente o mesmo layout do documento de origem. Essas traduções off-line funcionarão corretamente se os parágrafos não forem rearranjados. Se algum parágrafo for adicionado, dividido ou removido, o fluxo de texto após o parágrafo afetado será associado à cadeia de origem incorreta.

__Solução alternativa__: _não altere o número de parágrafos nem reorganize os parágrafos ao fazer a tradução off-line. Uma solução mais confiável é usar o editor da Web do Zanata em vez de traduzir off-line._

### Cadeias de Strings em documentos traduzidos são carregadas como traduções
Se você fizer o upload de um documento que seja traduzido apenas parcialmente, todas as strings de origem no documento serão tratadas como traduções aprovadas.

__Solução alternativa__: _faça o upload de documentos de tradução que são completamente traduzidos. Como alternativa, insira as traduções no editor da Web do Zanata para evitar o problema completamente._

### Dicas para traduzir documentos "Raw"
#### Tags Inline
Algumas partes de documentos raw não se destinam à tradução direta. Eles são convertidos em tags inline no estilo xml, como `<g1> <g2> </g2> </g1>`, no lugar da imagem no documento de exemplo. Recomenda-se que essas tags sejam incluídas nas traduções sem modificações.
