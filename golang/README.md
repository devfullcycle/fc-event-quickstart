# Instalação do Golang

Baixe o binário do Golang no link abaixo

https://go.dev/dl/

## Linux

Baixe executando o seguinte comando:

```bash
wget https://go.dev/dl/go1.20.4.linux-amd64.tar.gz
```

Remova qualquer instalação anterior do Go excluindo a pasta /usr/local/go (se existir) e extraia o arquivo que você acabou de baixar em /usr/local, criando uma nova árvore Go em /usr/local/go:

```bash
$ rm -rf /usr/local/go && tar -C /usr/local -xzf go1.20.4.linux-amd64.tar.gz
```

(Talvez seja necessário executar o comando como root ou através do sudo).

Não descompacte o arquivo em uma árvore /usr/local/go existente. Isso é conhecido por produzir instalações Go com erros.

Adicione /usr/local/go/bin à variável de ambiente PATH.
Você pode fazer isso adicionando a seguinte linha ao seu $HOME/.profile ou /etc/profile (para uma instalação em todo o sistema):
```bash
export PATH=$PATH:/usr/local/go/bin
```

Observação: as alterações feitas em um arquivo de perfil podem não ser aplicadas até a próxima vez que você fizer login no computador. Para aplicar as alterações imediatamente, basta executar os comandos shell diretamente ou executá-los a partir do perfil usando um comando como source $HOME/.profile.

Verifique se você instalou o Go abrindo um prompt de comando e digitando o seguinte comando:
```bash
$ go version
```

Confirme se o comando mostra a versão instalada do Go.

## Mac

Baixe a versão de acordo com o processador utilizado:

Para processadores ARM64, baixe o instalador no link abaixo

https://go.dev/dl/go1.20.4.darwin-amd64.pkg

Para processadores ADM64, baixe o instalador no link abaixo

https://go.dev/dl/go1.20.4.linux-amd64.tar.gz

Abra o arquivo do pacote que você baixou e siga as instruções para instalar o Go.
O pacote instala a distribuição Go em /usr/local/go. O pacote deve colocar o diretório /usr/local/go/bin em sua variável de ambiente PATH. Pode ser necessário reiniciar qualquer sessão aberta do Terminal para que a alteração entre em execução.

Verifique se você instalou o Go abrindo um prompt de comando e digitando o seguinte comando:

```bash
$ go version
```

Confirme se o comando imprime a versão instalada do Go.

## Windows/wsl

Pra a instalação no WSL, siga as instruções informadas para Linux


