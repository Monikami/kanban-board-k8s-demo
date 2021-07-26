This is the forked repository

Following commands are executed:

docker build -t kanban-app . 
docker tag kanban-app:latest 054242771358.dkr.ecr.ca-central-1.amazonaws.com/hello-world:kanban-app
docker push 054242771358.dkr.ecr.ca-central-1.amazonaws.com/hello-world:kanban-app
4c320d2a4c6d: Pushed
ceaf9e1ebef5: Pushed
9b9b7f3d56a0: Pushed
f1b5933fe4b5: Layer already exists
kanban-app: digest: sha256:aebc84ae423973f4ecdf300eff72ede9113f0dc17df625ac4861e36bf668ef0b size: 1159


HELM Chart created for kanban app and tested

helm install kanban-app kanban-app/ --values kanban-app/values.yaml
WARNING: Kubernetes configuration file is group-readable. This is insecure. Location: /root/.kube/config
WARNING: Kubernetes configuration file is world-readable. This is insecure. Location: /root/.kube/config
NAME: kanban-app
LAST DEPLOYED: Mon Jul 26 20:27:41 2021
NAMESPACE: default
STATUS: deployed
REVISION: 1
NOTES:
1. Get the application URL by running these commands:
  export POD_NAME=$(kubectl get pods --namespace default -l "app.kubernetes.io/name=kanban-app,app.kubernetes.io/instance=kanban-app" -o jsonpath="{.items[0].metadata.name}")
  export CONTAINER_PORT=$(kubectl get pod --namespace default $POD_NAME -o jsonpath="{.spec.containers[0].ports[0].containerPort}")
  echo "Visit http://127.0.0.1:8080 to use your application"
  kubectl --namespace default port-forward $POD_NAME 8080:$CONTAINER_PORT


 docker build -t kanban-ui .
docker tag kanban-ui:latest 054242771358.dkr.ecr.ca-central-1.amazonaws.com/hello-world:kanban-ui
 docker push 054242771358.dkr.ecr.ca-central-1.amazonaws.com/hello-world:kanban-ui
The push refers to repository [054242771358.dkr.ecr.ca-central-1.amazonaws.com/hello-world]
42a0e86f67ec: Layer already exists
84184a7a8f90: Layer already exists
fbe0fc9bcf95: Layer already exists
f1b5933fe4b5: Layer already exists
kanban-ui: digest: sha256:39229c5e90339d4598b6df5b154dfeb63df1f7fd632fd3055ff0e7ced6125360 size: 1157


helm install kanban-ui kanban-ui/ --values kanban-ui/values.yaml
WARNING: Kubernetes configuration file is group-readable. This is insecure. Location: /root/.kube/config
WARNING: Kubernetes configuration file is world-readable. This is insecure. Location: /root/.kube/config
NAME: kanban-ui
LAST DEPLOYED: Mon Jul 26 20:36:49 2021
NAMESPACE: default
STATUS: deployed
REVISION: 1
NOTES:
1. Get the application URL by running these commands:
  export POD_NAME=$(kubectl get pods --namespace default -l "app.kubernetes.io/name=kanban-ui,app.kubernetes.io/instance=kanban-ui" -o jsonpath="{.items[0].metadata.name}")
  export CONTAINER_PORT=$(kubectl get pod --namespace default $POD_NAME -o jsonpath="{.spec.containers[0].ports[0].containerPort}")
  echo "Visit http://127.0.0.1:8080 to use your application"
  kubectl --namespace default port-forward $POD_NAME 8080:$CONTAINER_PORT
[root@ip-172-31-10-105 example_env]# kubectl get pods -n default
NAME                          READY   STATUS             RESTARTS   AGE
kanban-app-56f8b776cf-x944q   0/1     CrashLoopBackOff   6          9m18s
kanban-ui-84dd7b9fb5-hvdt6    1/1     Running            0          10s

