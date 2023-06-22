Para o pacote do Kafka funcionar com o Golang, é necessário que a biblioteca C esteja disponível no Linux. Caso o erro abaixo ocorra, basta seguir os passos a seguir.
```
"internal/infra/kafka/consumer.go:6:20: undefined: ckafka.ConfigMap"
```
Ative a biblioteca do C nas variáveis de ambiente do Golang, executando este comando:
```
go env -w CGO_ENABLED=1
```
Se ocorrer o erro abaixo
```
cgo: C compiler "gcc" not found: exec: "gcc": executable file not found in $PATH
```
Basta instalar a biblioteca do C, com os seguintes comandos:
```
sudo apt update
sudo apt install build-essential
```
Com isto, o problema deve ser solucionado.