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
$ sudo rm -rf /usr/local/go && tar -C /usr/local -xzf go1.20.4.linux-amd64.tar.gz
```

Adicione /usr/local/go/bin à variável de ambiente PATH.

Você pode fazer isso executando um dos seguintes comandos:
```bash
# Para usuários que utilizam o Bash
echo 'export PATH=$PATH:/usr/local/go/bin' >> ~/.bashrc

# Para usuários que utilizam o Zsh
echo 'export PATH=$PATH:/usr/local/go/bin' >> ~/.zshrc

```

Observação: Para aplicar as alterações imediatamente, basta abrir uma nova instância no terminal.

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

https://go.dev/dl/go1.20.4.darwin-arm64.pkg

Abra o arquivo do pacote que você baixou e siga as instruções para instalar o Go.
O pacote instala a distribuição Go em /usr/local/go. O pacote deve colocar o diretório /usr/local/go/bin em sua variável de ambiente PATH. Pode ser necessário reiniciar qualquer sessão aberta do Terminal para que a alteração entre em execução.

Verifique se você instalou o Go abrindo um prompt de comando e digitando o seguinte comando:

```bash
$ go version
```

Confirme se o comando imprime a versão instalada do Go.

Caso o diretório /usr/local/go/bin não esteja em sua variável de ambiente PATH, execute um dos comandos abaixo:

```bash
# Para usuários que utilizam o Bash
echo 'export PATH=$PATH:/usr/local/go/bin' >> ~/.bashrc

# Para usuários que utilizam o Zsh
echo 'export PATH=$PATH:/usr/local/go/bin' >> ~/.zshrc

```

Observação: Para aplicar as alterações imediatamente, basta abrir uma nova instância no terminal.

## Windows/wsl

Para que você tenha uma boa experiência com as aulas, é importante que a instalação do Golang seja feita no WSL/Ubuntu. A instalação do Golang usando o executável para o Windows não trará os resultados esperados.

Portanto, para a instalação do Golang no WSL, siga as instruções informadas para Linux.
