https://www.cnblogs.com/uniqueDong/p/17443531.html

https://blog.csdn.net/weixin_42434700/article/details/146912634

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
