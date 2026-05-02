Kubernetes Demo — MongoDB + MongoExpress

What This Does
Deploys a multi-component app on Kubernetes:
- MongoDB (database)
- MongoExpress (database UI)

Components
- Secret — stores credentials
- ConfigMap — stores MongoDB URL
- MongoDB Deployment + ClusterIP Service
- MongoExpress Deployment + NodePort Service

How to Run
kubectl apply -f secrets.yml
kubectl apply -f mongo-configmap.yml
kubectl apply -f mongo.yml
kubectl apply -f mongoexpress.yaml

Access
minikube service mongoexpress-service --url
