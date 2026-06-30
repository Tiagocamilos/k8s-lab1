# Kubernetes Lab 1 - TodoList
![Kubernetes](https://img.shields.io/badge/Kubernetes-v1.28-326CE5?logo=kubernetes&logoColor=white)
![Kind](https://img.shields.io/badge/Kind-v0.20-000000?logo=kubernetes&logoColor=white)
![NGINX Ingress](https://img.shields.io/badge/NGINX%20Ingress-v1.8-009639?logo=nginx&logoColor=white)
![SQLite](https://img.shields.io/badge/SQLite-v3-003B57?logo=sqlite&logoColor=white)
![Docker](https://img.shields.io/badge/Docker-v24-2496ED?logo=docker&logoColor=white)
![cURL](https://img.shields.io/badge/cURL-v8-073551?logo=curl&logoColor=white)
![Node.js](https://img.shields.io/badge/Node.js-v18-339933?logo=node.js&logoColor=white)
![Express](https://img.shields.io/badge/Express-v4-000000?logo=express&logoColor=white)

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

- No documento sobre o lab1, o manifesto do CronJob.yml é referenciado a imagem abaixo:

```
curlimages/curl:8
```

Entretanto, essa tag não estava disponível no Docker Hub durante o desenvolvimento do laboratório. Foi utilizada a imagem:

```
curlimages/curl:8.16.0
```

que é compatível com o enunciado e permitiu a execução correta do CronJob.

## Para acessar o projeto Pelo Browser

``` http://todolist-grupo-02.local ```


