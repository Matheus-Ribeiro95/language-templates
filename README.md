## Templates em algumas linguagens de programação

Fiz esse repositório para mostrar o meu conhecimento em algumas linguagens de programação.
É um aplicativo simples e funcional.

Back-end: servidor API com chamadas GET e POST para ler/escrever do/no banco de dados (ScyllaDB). WebSocket para comunicação com o cliente. E um caminho estático para o arquivo HTML.

Front-end: tabela dinâmica utilizando jQuery e DataTables. Cliente WebSocket para receber dados do servidor quando alguma modificação for feita no banco de dados.

> TODO: fazer front-end em Angular, React e Vue.
___

Linguagens utilizadas: JavaScript, Python, Go, Java, Rust e PHP.
___

Disponível em arquivo Kubernetes e chart Helm.

## Go

    kubectl apply -f kubernetes.gotemplate.yaml

Depois do pod estar executando:

    kubectl port-forward POD_NAME 8080

Acesse [localhost:8080/static](localhost:8080/static)
