## Instalação Docker

É importante que tudo o que formos instalar para fins de desenvolvimento e um melhor acompanhamento do curso seja instalado dentro do `WSL`, enquanto estivermos desenvolvendo pense apenas no `WSL (Linux)`.

## Windows

---

Um passo importantes antes de iniciar a instalação do `Docker` é verificar se não há alguma atualização do `Windows` pendente, para isso acesse `Configurações` e vá até o menu do `Windows Update`, confirme se existe alguma atualização a ser realizada, é importante manter o `Windows` atualizado, pois isso irá manter o `WSL` sempre com as últimas atualizações.

---

Não é recomendado a utilização do `Docker Desktop`, além de consumir muita memória `RAM` (Aproximadamente 2GB) e impactar em uma pequena parte de consumo do `CPU`.
Percebemos uma diferença significativa de performance e um ponto importante é que ele não é compatível com `host.docker.internal` e durante nosso curso vamos utilizar o `host.docker.internal` para realizar a comunicação entre os `containers`.

Abaixo um vídeo sobre o Porque não é recomendado o uso do Docker Desktop.

### Link: https://www.youtube.com/watch?v=wpdcGgRY5kk

A única opção para utilizar o `Docker Desktop` é no seguinte cenário: quando precisamos trabalhar com `containers Windows` para `.NET` ou funcionalidades referente a `Microsoft`, veja que são casos específicos.

---

## Outras distros Linux

Para realizar a intalação do `Docker` em outras distro `Linux` veja o link abaixo e siga os passos recomendados pela documentação oficial:

### Link: https://docs.docker.com/engine/install/#server

---

## Windows 10

Pra termos bons resultados em relação às aulas, é importante usar o Docker Engine. Caso tenha instalado o Docker Desktop, por favor, desinstale e siga a instruções abaixo para instalação do Docker Engine na distruibição Linux Ubuntu. 

Desinstale todas as versões anteriores com o seguinte comando:

```bash
sudo apt-get remove docker docker-engine docker.io containerd runc
```

1 - Agora instale os pacotes necessários para a isntalação:

```bash
sudo apt-get update
sudo apt-get install ca-certificates curl gnupg
```

2 - Adicione a GPG key oficial do Docker:

```bash
sudo install -m 0755 -d /etc/apt/keyrings
curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo gpg --dearmor -o /etc/apt/keyrings/docker.gpg
sudo chmod a+r /etc/apt/keyrings/docker.gpg
```

3 - Set o repositório com o comando abaixo:

```bash
echo \
  "deb [arch="$(dpkg --print-architecture)" signed-by=/etc/apt/keyrings/docker.gpg] https://download.docker.com/linux/ubuntu \
  "$(. /etc/os-release && echo "$VERSION_CODENAME")" stable" | \
  sudo tee /etc/apt/sources.list.d/docker.list > /dev/null
```

4 - Execute a apt update:

```bash
sudo apt-get update
```

5 - Instale a versão mais atual

```bash
sudo apt-get install docker-ce docker-ce-cli containerd.io docker-buildx-plugin docker-compose-plugin
```

6 - Teste executando o comando abaixo

```bash
sudo docker run hello-world
```

Depois de instalado, execute os seguinte passos para remover a necessidade de rodar o docker com sudo:

1 - Crie o grupo docker.
```bash
sudo groupadd docker
```

2 - Adicione o seu usuário no grupo docker

```bash
sudo usermod -aG docker $USER
```

3 - Execute o seguinte comando para ativar as mudanças de grupos

```bash
newgrp docker
```

4 - Rode o comando sem o sudo:

```bash
docker run hello-world
```

Observação importante: Sempre que iniciarmos o `WSL (Linux)`, precisamos rodar o comando: `sudo service docker start`

---

Possível erro ao iniciar o `Docker` no `Ubuntu 22.04`

Se ao tentar iniciar o `Docker` e receber o seguinte erro:

` Cannot connect to the Docker daemon at unix:///var/run/docker.sock. Is the docker daemon running? `

Rode o comando: `sudo update-alternatives --config iptables` e escolha a opção 1 `iptables-legacy`.

Rode novamente o comando: `sudo service docker start` e teste com o comando: `docker ps`, caso não receba mais nenhum erro tudo estará correto.

---

## Windows 11
        - Criar o `/etc/wsl.conf` -> [boot] command = sudo service docker start (olhar no tutorial)
    # recomendado transferir os projetos da C: para o /home/SEU_USER e novos projetos devem ser criados dentro do sistema de arquivos do Linux na pasta /home (acrescente trecho de live sobre como fazer backup e restauração do WSL)
    # instalação da extensão WSL do VSCode
        - explicar que se o projeto não foi aberto no modo Remote WSL, o VSCode perderá performance e não conseguirá enxergar o projeto totalmente
    # recomendação de uso Windows Terminal

# Linux

Pra termos bons resultados em relação às aulas, é importante usar o Docker Engine. Caso tenha instalado o Docker Desktop, por favor, desinstale e siga a instruções abaixo para instalação do Docker Engine na distruibição Linux Ubuntu. 

Desinstale todas as versões anteriores com o seguinte comando:

```bash
sudo apt-get remove docker docker-engine docker.io containerd runc
```

1 - Agora instale os pacotes necessários para a isntalação:

```bash
sudo apt-get update
sudo apt-get install ca-certificates curl gnupg
```

2 - Adicione a GPG key oficial do Docker:

```bash
sudo install -m 0755 -d /etc/apt/keyrings
curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo gpg --dearmor -o /etc/apt/keyrings/docker.gpg
sudo chmod a+r /etc/apt/keyrings/docker.gpg
```

3 - Set o repositório com o comando abaixo:

```bash
echo \
  "deb [arch="$(dpkg --print-architecture)" signed-by=/etc/apt/keyrings/docker.gpg] https://download.docker.com/linux/ubuntu \
  "$(. /etc/os-release && echo "$VERSION_CODENAME")" stable" | \
  sudo tee /etc/apt/sources.list.d/docker.list > /dev/null
```

4 - Execute a apt update:

```bash
sudo apt-get update
```

5 - Instale a versão mais atual

```bash
sudo apt-get install docker-ce docker-ce-cli containerd.io docker-buildx-plugin docker-compose-plugin
```

6 - Teste executando o comando abaixo

```bash
sudo docker run hello-world
```

Depois de instalado, execute os seguinte passos para remover a necessidade de rodar o docker com sudo:

1 - Crie o grupo docker.
```bash
sudo groupadd docker
```

2 - Adicione o seu usuário no grupo docker

```bash
sudo usermod -aG docker $USER
```

3 - Execute o seguinte comando para ativar as mudanças de grupos

```bash
newgrp docker
```

4 - Rode o comando sem o sudo:

```bash
docker run hello-world
```

## Outras distros Linux

Para realizar a intalação do `Docker` em outras distro `Linux` veja o link abaixo e siga os passos recomendados pela documentação oficial:

### Link: https://docs.docker.com/engine/install/#server


# Mac

    - Instalar o Docker Desktop ou M1/M2 ou pra Intel 
