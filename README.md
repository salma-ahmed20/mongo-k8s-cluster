
# Mongo-k8s-cluster
Deploy Mongodb and MongoExpress on kubernetes cluster

## What is MongoExpress
It is an interactive lightweight Web-Based Administrative Tool to effectively manage (MongoDB) Databases. Written with Node.js, Express, and Bootstrap3, Mongo Express can be used to simplify several MongoDB Admin tasks. Using MongoExpress, you can add, delete or modify databases, collections, and documents.

## What is MongoDB 
It is a NoSQL Open-source Document Oriented Database developed for storing and processing high volumes of data

## Prerequisite:
- Minikube cluster running

## Demo executed - Deploying MongoDB and MongoExpress:
- Created MongoDB Deployment
- Created Secret for Mongo Credentials
- Created MongoDB Internal Service
- Created MongoExpress Deployment
- Created ConfigMap for DB Server URL
- Created MongoExpress External Service

## kubectl apply commands in order

```javascript
kubectl apply -f mongo-secret.yaml
kubectl apply -f mongo.yaml
kubectl apply -f mongo-configmap.yaml 
kubectl apply -f mongo-express.yaml
```

## kubectl get commands
```javascript
kubectl get pod
kubectl get pod --watch
kubectl get pod -o wide
kubectl get service
kubectl get secret
kubectl get all | grep mongodb
```

## kubectl debugging commands
```javascript
kubectl describe pod mongodb-deployment-xxxxxx
kubectl describe service mongodb-service
kubectl logs mongo-express-xxxxxx
```


## give a URL to external service in minikube
- mandatory if you use minikube
```javascript
minikube service mongo-express-service
```
