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


    - seguir os comandos de instalação para Ubuntu
    - explicar e apontar onde encontram os comandos para outras distribuições

    # windows 10
        - toda vez que iniciar o WSL, precisa rodar o comando `sudo service docker start`
    # windows 11
        - Criar o `/etc/wsl.conf` -> [boot] command = sudo service docker start (olhar no tutorial)
    # recomendado transferir os projetos da C: para o /home/SEU_USER e novos projetos devem ser criados dentro do sistema de arquivos do Linux na pasta /home (acrescente trecho de live sobre como fazer backup e restauração do WSL)
    # instalação da extensão WSL do VSCode
        - explicar que se o projeto não foi aberto no modo Remote WSL, o VSCode perderá performance e não conseguirá enxergar o projeto totalmente
    # recomendação de uso Windows Terminal

# Linux

    - não recomendação do Docker Desktop
        - consume 2GB
        - miudeza de CPU
        - performance
        - host.docker.internal
    - seguir os comandos de instalação para Ubuntu
    - explicar e apontar onde encontram os comandos para outras distribuições


# Mac

    - Instalar o Docker Desktop ou M1/M2 ou pra Intel 
