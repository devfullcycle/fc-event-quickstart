## Instalação Node.Js

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

Caso a saída for diferente da versão do `nvm` ou um erro verifique o arquivo do `shell` como o exemplo abaixo:

bash: `vim ~/.bashrc`

zsh: `vim ~/.zshrc`

Dentro do arquivo deve conter a seguinte informação:

```
export NVM_DIR="$([ -z "${XDG_CONFIG_HOME-}" ] && printf %s "${HOME}/.nvm" || printf %s "${XDG_CONFIG_HOME}/nvm")"
[ -s "$NVM_DIR/nvm.sh" ] && \. "$NVM_DIR/nvm.sh" # This loads nvm
```

Se o conteúdo acima não estiver no arquivo execute este comando acima em um terminal para incluir a variável de ambiente do `nvm`.

---

Agora para instalarmos a versão `19` do `Node.js` que utilizaremos no curso, vamos abrir o terminal e executar o comando:

`nvm install 19`

Ele irá baixar a versão que escolhemos acima, então vamos verificar a instalação:

No terminal:

`nvm ls`

Veremos a versão `19` listada.

Para utilizar a versão `19` rode o comando:

`nvm use 19`

E para deixar esta versão como `default` rode o comando:

`nvm alias default 19`

Com isso todas as vezes que for utilizar o `node` a versão `19` será utilizada.

---

#### Erros comuns no Linux:

Caso o comando `nvm --version` retorne o erro: `nvm: command not found`, feche o terminal e abra novamente ou execute o comando baseado em seu `shell` exemplo:

bash: `source ~/.bashrc`

zsh: `source ~/.zshrc`

