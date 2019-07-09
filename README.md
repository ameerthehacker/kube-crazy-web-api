# Crazy Web API

:hammer: A demo project to run a simple .NET Core Web API in Kubernetes

## Deploying to MiniKube

1. Point docker client to the minikube docker server

```sh
$ eval $(minikube docker-env)
```

2. Building the docker image

```sh
$ docker-compose build
```

3. Test locally using docker-compose

```sh
$ docker-compose up
```

4. Deploy the pod, replica or the service

```sh
$ kubectl apply -f <path-to-config.yml>
```

5. Check it in the Kube dashboard

```sh
$ minikube dashboard
```

## Handy commands

### Get the minikube ip

```sh
$ minikube ip
```

### List a resource in Kubernetes

```sh
$ kubectl get pod --namespace=<your-namespace>
```

In general it is

```sh
$ kubectl get <resource> --namespace=<your-namespace>
```

### Delete a resource in Kubernetes

```sh
$ kubectl delete <resource> --namespace=<your-namespace>
```

### View the Kube dashboard

```sh
$ minikube dashboard
```

### View list of available contexts (conneted clusters)

```sh
$ kubectl config get-contexts
```
