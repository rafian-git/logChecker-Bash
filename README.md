# logChecker-Bash
takes in service name and checks log of that kubernetes pod

### usage
```service="auth" ./logChecker.sh```

### response
``` β³auth
β More than one pod found
π Checking pods' status
π 1 : auth-696945c8c9-gt65j - Running
π 2 : auth-696945c8c9-h9wxx - Failed
π 3 : auth-696945c8c9-qcgfv - Failed
π 4 : auth-696945c8c9-tbch4 - Failed
π 5 : redis-0 - Running
input number (1-5) to check logs of that pod : 1
β Pod is running - showing logs below
W1031 13:03:37.418811   75869 gcp.go:119] WARNING: the gcp auth plugin is deprecated in v1.22+, unavailable in v1.26+; use gcloud instead.
To learn more, consult https://cloud.google.com/blog/products/containers-kubernetes/kubectl-auth-changes-in-gke
1.667122453229934e+09   info    auth    log/logger.go:98        nats not connected. Trying to connect ...
1.6671224532302306e+09  error   auth    log/logger.go:116       dial tcp [::1]:4222: connect: cannot assign requested address
1.6671224582296932e+09  info    auth    log/logger.go:98        nats not connected. Trying to connect ...
1.6671224582302701e+09  error   auth    log/logger.go:116       nats: no servers available for connection
................
```

