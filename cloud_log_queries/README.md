# Cloud Log Queries

## When there's availability alert

### Uptime Check
```
https://console.cloud.google.com/monitoring/uptime/mesh-ingress-api-prd-sdp-wpesvc-net?project=wp-engine-corporate-prod
```

### Gateway log query
```
resource.type="k8s_container"
resource.labels.namespace_name="ingress"
"GET /status"
-"200"
```

### Status Service query
```
resource.type="k8s_container"
resource.labels.namespace_name="status-service"
-"200"
```