https://www.cnblogs.com/uniqueDong/p/17443531.html

https://blog.csdn.net/weixin_42434700/article/details/146912634

## Install redis in k8s
This is an installation guide.You'll learn how to install,run,and experiment with the Redis server process.

## How to install redis operator in k8s
```
helm repo add ot-helm https://ot-container-kit.github.io/helm-charts/
helm repo update

helm upgrade --install redis-operator ot-helm/redis-operator \
  --namespace ot-operators \
  --create-namespace \
  --version 0.23.0   # 可省略，使用最新版（2026 年最新 ≈0.23.x 或更高，检查 helm search repo redis-operator）
```

## Query redis
```
KEYS pattern*
SCAN 0 MATCH pattern* COUNT 100
EXISTS key
TYPE key
TTL key
```
## Delete
```
DEL key
UNLINK key     # 非阻塞删除（生产环境推荐）
```

## Expire
```
EXPIRE key 3600
PERSIST key
```
