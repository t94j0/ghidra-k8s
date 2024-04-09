# Adding Users

```bash
USER="john44"
kubectl exec -ti ghidra-0 -- /bin/bash -c "cd /ghidra/server && ./svrAdmin -add ${USER}"
```
