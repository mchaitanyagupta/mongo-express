# mongo-express


catch that if you can

1-deployment of mongodb
2-adding service to the deployment to communicate
    only communicate with in the cluster no target port 
3-adding secret to the key value pairs for username and password
4-adding deployment of mongo-express to talk with database
5-adding service to take requests from outside the cluster
6-configmap to configure the database url for mongo-express
    removing the hardcoding of mongodb_server value with valuefrom secretkey name and value

commands:
  kubectl apply -f secret.yaml
  kubectl apply -f mongodb.yaml
  kubectl apply -f confingmap.yaml
  kubectl apply -f mongo-express.yaml
  general commands used:
    kubectl get po(for pods)
    kubectl het no(for nodes)
    kubectl get svc(for services)
    kubectl get all
    kubectl log podname
    kubectl describe pod podname
    minikube service mongo-express-service
    minikube service list
    kubectl edit deployment mongo-express


minkube from the docker container instead of hyperkit
kubectl have dependency to minikube
docker desktop
vs code
flow:
  request to mongo-express-service from browser
  forwarded to mongo-express pod
  the talks to mongodb-service
  then to actual db mongodb pod
try adding ingress to the service of the mongo-express-service
    
    
