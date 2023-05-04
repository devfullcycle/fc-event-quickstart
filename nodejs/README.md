## Instalação Node.Js

Primeiro precisamos instalar um gerenciador de versões do `node.js` que neste caso será o `nvm`.

---
### Linux / MacOS / Windows (WSL):

---

Para instalar o `nvm` precisamos executar um `script` de instalação como abaixo:

```
curl -o- https://raw.githubusercontent.com/nvm-sh/nvm/v0.39.3/install.sh | bash
```

Abra um terminal e rode o comando abaixo para verificar se a instalação está correta:

`nvm --version`

A saída do terminal deve ser a versão do `nvm`.

---

Agora para instalarmos a versão `19` do `Node.js` que utilizaremos no curso, vamos abrir o terminal e executar o comando:

`nvm install 19`

Ele irá baixar a versão que escolhemos acima, então vamos verificar a instalação:

No terminal:

`nvm ls`

Veremos a versão `19` listada.

---

#### Erros comuns no Linux:

Caso o comando `nvm --version` retorne o erro: `nvm: command not found`, feche o terminal e abra novamente ou execute o comando baseado em seu `shell` exemplo:

bash: `source ~/.bashrc`

zsh: `source ~/.zshrc`

