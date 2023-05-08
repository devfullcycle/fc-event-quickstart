
# ressaltar a importância do WSL para o uso do Docker

# windows
    - recomendar a atualização do Windows via Windows Update para sempre receber as últimas atualizações do WSL.
    - não recomendação do Docker Desktop
        - consume 2GB
        - miudeza de CPU
        - performance
        - host.docker.internal
        - https://www.youtube.com/watch?v=wpdcGgRY5kk (Porque Docker Desktop não é recomendado)
        - único é se você precisa de containers Windows para .net ou coisas da microsoft
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
