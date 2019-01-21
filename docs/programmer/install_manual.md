Se você quiser configurar o zanata-cli manualmente (sem o 0install):

1. Navegue até [zanata-cli no Maven Central](http://search.maven.org/#search%7Cga%7C1%7Cg%3A%22org.zanata%22%20AND%20a%3A%22zanata-cli%22) .
1. Baixar seja `dist.zip` ou `dist.tar.gz`.
1. Extraia o conteúdo do arquivo para o local de sua escolha.
1. Crie um link simbólico para o script `zanata-cli` no diretório bin do archive extraído. Por exemplo, a partir do diretório do arquivo, execute `sudo ln -s --relative bin/zanata-cli /usr/local/bin/zanata-cli`.
1. (opcional) você também pode habilitar o preenchimento automático de tabulação para o cliente se você usar o bash como seu terminal shell. Isso pode ser feito copiando ou vinculando o `zanata-cli-completion` do diretório `bin` para `/etc/bash_completion.d/` por exemplo `ln -s --relative bin/zanata-cli-completion /etc/bash_completion.d/zanata-cli-completion`.