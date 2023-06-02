## Instalação Node.Js

É importante que tudo o que formos instalar para fins de desenvolvimento e um melhor acompanhamento do curso seja instalado dentro do `WSL`, enquanto estivermos desenvolvendo pense apenas no `WSL (Linux)`.

Primeiro precisamos instalar um gerenciador de versões do `node.js` que neste caso será o `nvm`.

---
### Linux / MacOS / Windows (WSL):

---

Para instalar o `nvm` precisamos executar um `script` de instalação como abaixo:

```
curl -o- https://raw.githubusercontent.com/nvm-sh/nvm/v0.39.3/install.sh | bash
```

Após executar o comando acima feche o terminal e abra um novo terminal e rode o comando abaixo para verificar se a instalação está correta:

`nvm --version`

A saída do terminal deve ser a versão do `nvm`.

Caso a saída for diferente da versão do `nvm` ou recebermos um erro verifique o arquivo do `shell` como o exemplo abaixo:

Caso utilize o terminal `bash` padrão do `WSL` rode o comando abaixo:

bash: `cat ~/.bashrc`

Caso utilize o terminal `oh-my-zsh` rode o comando abaixo:

zsh: `cat ~/.zshrc`

A saída do comando acima deve conter a seguinte informação:

```
export NVM_DIR="$([ -z "${XDG_CONFIG_HOME-}" ] && printf %s "${HOME}/.nvm" || printf %s "${XDG_CONFIG_HOME}/nvm")"
[ -s "$NVM_DIR/nvm.sh" ] && \. "$NVM_DIR/nvm.sh" # This loads nvm
```

Se o conteúdo acima não estiver no arquivo execute este comando abaixo e vamos incluir a variável de ambiente do `nvm`.

Caso utilize o terminal `bash` padrão do `WSL` rode o comando abaixo, confirme se o terminal que será executado os comandos abaixo de instalação é o correto `(bash)`:

bash: `code ~/.bashrc`

Inclua ao final do arquivo o seguinte código:

```
export NVM_DIR="$([ -z "${XDG_CONFIG_HOME-}" ] && printf %s "${HOME}/.nvm" || printf %s "${XDG_CONFIG_HOME}/nvm")"
[ -s "$NVM_DIR/nvm.sh" ] && \. "$NVM_DIR/nvm.sh" # This loads nvm
```

Caso utilize o terminal `oh-my-zsh` rode o comando abaixo confirme se o terminal que será executado os comandos abaixo de instalação é o correto `(oh-my-zsh (zsh))`.:

zsh: `code ~/.zshrc`

Inclua ao final do arquivo o seguinte código:

```
export NVM_DIR="$([ -z "${XDG_CONFIG_HOME-}" ] && printf %s "${HOME}/.nvm" || printf %s "${XDG_CONFIG_HOME}/nvm")"
[ -s "$NVM_DIR/nvm.sh" ] && \. "$NVM_DIR/nvm.sh" # This loads nvm
```

---

Agora para instalarmos a versão `20` do `Node.js` que utilizaremos no curso, vamos abrir o terminal e executar o comando:

`nvm install 20`

Ele irá baixar a versão que escolhemos acima, então vamos verificar a instalação:

No terminal:

`nvm ls`

Veremos a versão `20` listada.

Para utilizar a versão `20` rode o comando:

`nvm use 20`

E para deixar esta versão como `default` rode o comando:

`nvm alias default 20`

Com isso todas as vezes que for utilizar o `node` a versão `20` será utilizada.

---

#### Erros comuns no Linux:

Caso o comando `nvm --version` retorne o erro: `nvm: command not found`, feche o terminal e abra novamente ou execute o comando baseado em seu `shell` exemplo:

bash: `source ~/.bashrc`

zsh: `source ~/.zshrc`

