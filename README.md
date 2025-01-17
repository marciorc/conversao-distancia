# conversao-distancia

## Link do Docker-Hub
https://hub.docker.com/repository/docker/marcioramoscorrea/conversao-distancia/

## Aula 1 - Docker
### Comandos Importantes
- `docker build -t conversao-distancia -f Dockerfile .`  
Cria a imagem a partir da receita descrita no Dockerfile  

- `docker container run -d -p 8181:5000 conversao-distancia`  
Executa o container passando os seguintes parametros  
-d = daemon  
-p = port  

- `docker image prune`
Limpa as imagens residuais

## Aula 2 - Kubernetes
### Comandos Importantes
- `k3d cluster create {{meucluster}} --servers 3 --agents 3`
Cria um cluster com servers e agents
    - `k3d cluster create {{meucluster}} --servers 1 --agents 2 -p "8080:30000@loadbalancer"`
    Cria um cluster com servers e agents fazendo o publish da porta parametrizada


- `kubectl get nodes`
Lista os nodes ativos

- `k3d cluster list`
Lista os clusters ativos

- `k3d cluster delete {{meucluster}}`
Deleta cluster criado com o nome passado por parametro

- `kubectl api-resources`
Lista os recursos do kubernets

- `kubectl apply -f k8s/deployment.yml`
Aplica as condições listadas no deployment.yml

- `kubectl get pods`
Lista os pods
    - `kubectl get pods -o wide`
    Lista os pods exibindo mais detalhes

- `kubectl describe pod {{pod_name}}`
Exibe todas descrições do Pod

- `kubectl get replicaset`
Lista os controladores de pods ativos
    -`kubectl get replicaset,pod`
    Lista os controladores de pods e pods ativos

- `kubectl apply -f k8s/deployment.yml && watch 'kubectl get pod'`
Aplica as condições listadas no deployment.yml e lista os pods criados em tempo real

- `kubectl delete pod {{pod_name}} && watch 'kubectl get pod'`
Deleta o Pod e lista o pod deletado em tempo real

- `kubectl port-forward pod/{{pod_name}} 8080:5000`
Faz o direcionamento das portas

- `kubectl get all`
Lista todos recursos ativos do k8s

- `kubectl rollout history deployment {{app_name}}`
Lista as mudanças de versões

- `kubectl rollout und deploymet {{app_name}}`
Retorna a versão anterior

### Anotações
- **pod**: menor objeto do cluster kubernetes, onde é executado os containers
- **replicaset**: Cuida da escalabilidade e resiliência dos pods. Controlador dos pods.
- **deployment**: Faz o gerenciamento do ReplicaSet;
- **service**: serve para expor a aplicação presente nos pods.

Toda vez que há uma atualização da aplicação, é gerado um novo **replicaset**.

## Aula 3 - AWS
### Comandos Importantes
- `aws configure`
Comando para configurar o access key e secret key do user.

- `aws eks update-kubeconfig --name {{eks-name}}`

### Anotações



## Aula 4 - Github Actions
### Comandos Importantes

### Anotações




## Aula 5 - Prometheus e Grafana
### Comandos Importantes

### Anotações