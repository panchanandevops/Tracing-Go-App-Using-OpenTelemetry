# Tracing-Go-App-Using-OpenTelemetry
"Effortlessly trace and visualize your Golang app's performance! Utilizing OpenTelemetry and Tempo, capture distributed traces for deep system insights. View dynamic Grafana dashboards to track performance and dependencies with ease. Elevate monitoring with Tracing-Go-App-Using-OpenTelemetry!"




## Commands from the Tutorial

```bash
git clone git@github.com:antonputra/tutorials.git
cd tutorials/lessons/178
cd terraform
terraform init
terraform apply
cd ..
cd myapp
go mod tidy
kubectl get pods -n monitoring
kubectl port-forward svc/tempo 4318 -n monitoring
export OTLP_ENDPOINT=localhost:4318
curl http://0.0.0.0:8080/devices
kubectl port-forward svc/grafana 3000:80 -n monitoring
# Datasource URL: http://tempo.monitoring:3100
kubectl apply -f k8s
kubectl get pods -n default
kubectl get svc -n default
kubectl port-forward svc/myapp 8080:8080 -n default
```