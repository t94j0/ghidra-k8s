# Installing

```bash
# Add Helm repo
helm repo add ghidra http://www.maxh.io/ghidra-k8s
# Install Ghidra
helm install myghidra ghidra/ghidra
```

If you need to modify values.yaml:

```bash
# Add the repo first, then continue with the following steps
helm show values ghidra/ghidra > /tmp/values.yaml
# Install with values.yaml
helm install ghidra/ghidra -f /tmp/values.yaml
```

# Adding Users

```bash
USER="john44"
kubectl exec -ti ghidra-0 -- /bin/bash -c "cd /ghidra/server && ./svrAdmin -add ${USER}"
```

# Acknowledgements

- [Blacktop's Ghidra Docker Container](https://github.com/blacktop/docker-ghidra)
