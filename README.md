# mykind

## Pré-requisitos

Para usar o `Kind` na sua máquina, instale os binários abaixo:

1. kubectl
2. kind
3. helm
4. flux

## Criação do cluster

Abra o terminal e se deloque para a pasta raiz deste repositório.

```
$ kind create cluster --name [NOME DO CLUSTER] --config config.yaml
```

Verfique se os nós criados já estão com o status `Ready`

```
$ kubectl get nodes
```

## Instalação do flux no cluster

```
flux install
kubectl get pod -A | grep flux
kubectl get crds | grep fluxcd
kubectl api-resources | grep fluxcd

