## Templates em algumas linguagens de programação

Fiz esse repositório para mostrar o meu conhecimento em algumas linguagens de programação.
É um aplicativo simples e funcional.

Back-end: servidor API com chamadas GET e POST para ler/escrever do/no banco de dados (ScyllaDB). WebSocket para comunicação com o cliente. E um caminho estático para o arquivo HTML.

Front-end: tabela dinâmica utilizando jQuery e DataTables. Cliente WebSocket para receber dados do servidor quando alguma modificação for feita no banco de dados.

> TODO: fazer front-end em Angular, React e Vue.
___

Linguagens utilizadas: [JavaScript](#javascript-com-typescript), [Python](#python), [Go](#go), [Java](#java), [Rust](#rust) e [PHP](#php).
___

Disponível em arquivo Kubernetes e [chart Helm](#chart-helm).

## JavaScript com TypeScript

    kubectl apply -f kubernetes.jstemplate.yaml

Depois do pod estar executando:

    kubectl port-forward POD_NAME 8080

Acesse [localhost:8080/static](http://localhost:8080/static/index.html)

## Python

    kubectl apply -f kubernetes.pytemplate.yaml

Depois do pod estar executando:

    kubectl port-forward POD_NAME 8000

Acesse [localhost:8000/static](http://localhost:8000/static/index.html)

## Go

    kubectl apply -f kubernetes.gotemplate.yaml

Depois do pod estar executando:

    kubectl port-forward POD_NAME 8080

Acesse [localhost:8080/static](http://localhost:8080/static/index.html)

## Java

    kubectl apply -f kubernetes.javatemplate.yaml

Depois do pod estar executando:

    kubectl port-forward POD_NAME 8080

Acesse [localhost:8080](http://localhost:8080)

## Rust

    kubectl apply -f kubernetes.rstemplate.yaml

Depois do pod estar executando:

    kubectl port-forward POD_NAME 3000 8080 9000

Acesse [localhost:3000](http://localhost:3000)

## PHP

    kubectl apply -f kubernetes.phptemplate.yaml

Depois do pod estar executando:

    kubectl port-forward POD_NAME 8080 8081

Acesse [localhost:8080/static](http://localhost:8080/static)

## Chart Helm

Configurando o repositório:

    helm repo add matheus-ribeiro95 https://matheus-ribeiro95.github.io/helm-charts

Atualize o repositório

    helm repo update

Para instalar

    helm install NOME_RELEASE matheus-ribeiro95/
    ---
    TAB para ver as opções
    Escolha o chart

Depois do pod estar executando:

    kubectl port-forward POD_NAME PORTAS
    ---
    PORTAS varia para cada linguagem

 - Javascript: 8080
 - Python: 8000
 - Go: 8080
 - Java: 8080
 - Rust: 3000 8080 9000
 - PHP: 8080 8081
