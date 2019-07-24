# web-k8s-exec

Use WebSocket implements Docker exec via Kubernetes API.

## Getting and Start

```
git clone https://github.com/samejack/web-k8s-exec.git
cd web-k8s-exec
npm install
nodejs index.js
```
You can change configuration in index.js

### token

Grab default-token here. replace with your configuration like admin-user
```
kubectl -n kube-system describe secret $(kubectl -n kube-system get secret | grep default | awk '{print $1}')
```

### host

Check ```~/.kube/config``` for API endpoint

ex: ```https://192.168.0.1:6443```

set the host in index.js like ```wss://192.168.0.1:6443```

## Use browser goto http://127.0.0.1:8080

Screenshot
![Alt Screenshot](https://github.com/samejack/web-k8s-exec/raw/master/example/web-k8s-exec.png)

## License

Apache License Version 2.0
