# Kubernetes Lab 1 - TodoList

Laboratório desenvolvido utilizando Kubernetes (Kind) para implantação da aplicação TodoList.

## Baixar o Projeto
```git clone https://github.com/Tiagocamilos/k8s-lab1.git ```

## Entrar no Projeto
```cd k8s-lab1 ```

# Executar

## Ordem de aplicação dos manifestos

```bash
kubectl apply -f namespace.yaml
kubectl apply -f configmap.yaml
kubectl apply -f secret.yaml
kubectl apply -f pvc.yaml
kubectl apply -f deployment.yaml
kubectl apply -f service.yaml
kubectl apply -f ingress.yaml
kubectl apply -f cronjob.yaml
```

## Observações

- O Ingress foi configurado utilizando o host:

```
todolist-grupo-02.local
```

Adicione ao arquivo `/etc/hosts`:

```
127.0.0.1 todolist-grupo-02.local
```

- O enunciado especifica a imagem:

```
curlimages/curl:8
```

Entretanto, essa tag não estava disponível no Docker Hub durante o desenvolvimento do laboratório. Foi utilizada a imagem:

```
curlimages/curl:8.16.0
```

que é compatível com o enunciado e permitiu a execução correta do CronJob.

## Para acessar o projeto Pelo Browser

``` 127.0.1.1 todolist-grupo-02.local ```


