---
title: Anotações sobre Kubernetes
date: 2021-07-17T20:13:35-03:00
category: Cloud
tags: docker, kubernetes, devops
---

## Tutoriais
- https://kubernetes.io/pt-br/docs/tutorials/kubernetes-basics/
- https://dzone.com/articles/kubernetes-in-10-minutes-a-complete-guide-to-look
- https://dev.to/stevenmcgown/kubernetes-for-dummies-5hmh 
- Cheatsheet: https://kubernetes.io/docs/reference/kubectl/cheatsheet/

## Definições
- **K8s**: Abreviação de "kubernetes" (8 letras do meio);
- **Cluster**: Conjunto de servidores, chamados "nós";
- **Pod**: É o menor objeto no k8s. Representa um grupo de contêineres. Um nó possui um ou mais pods;
- **Minikube**: Versão leve do k8s para uso local;
- **kubectl**: Aplicação para enviar comandos ao k8s;

## Comandos
  - **kubectl**
    - **version**: retorna a versão do cliente e do servidor. O "cliente" é o próprio kubectl. Os dados do servidor se referem ao K8s instalado no nó master;
    - **cluster-info**: visualizar informações do *cluster*;
    - **logs**: exibe logs do container no pod que forem exibidos na saída padrão;
    - **get nodes**: visualizar informações dos nós;
    - **delete service (service)**
    - **delete deployment (name)**
  - **minikube**
    - **start**: iniciar um cluster
    - **dashboard**: abre uma página web para gerenciamento do k8s;
    - **stop**
    - **delete**

## Observações
- Tipos possíveis no kind: Pod, ReplicaSet, ReplicationController, Deployment e Service
- Os filtros são aplicados nos labels
- Dentro de "labels" podem ser adicionadas chaves personalizadas
- Para adicionar imagens locais do docker no arquivo yaml:
  - Executar `eval $(minikube docker-env)`
  - Na seção de configuração do container, adicionar `imagePullPolicy: IfNotPresent`
  - Executar o minikube com flag insecure: `minikube start --insecure-registry`
  - 



