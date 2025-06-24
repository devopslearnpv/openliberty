
 Step 1: Create Namespace + Quota + Limit
 kubectl apply -f demo-simple-namespace.yaml

 Step 2: Create ConfigMap
 kubectl apply -f hello-configmap.yaml
 
 Step 3: Create Deployment
 kubectl apply -f hello-deployment.yaml

 Step 4: Create Service
 kubectl apply -f hello-service.yaml

 Step 5 : Validation
                Run: kubectl get all -n demo-simple
                      Forward the port: kubectl port-forward svc/hello-svc 8080:80 -n demo-simple
                      Test with curl: curl http://localhost:8080
