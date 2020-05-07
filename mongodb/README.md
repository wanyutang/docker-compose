# fun3w/mongodb

- [30-2之使用Docker來建構MongoDB環境](https://ithelp.ithome.com.tw/articles/10184657)
- [Dokcer Mongo 初始化權限設定 學習手雜](https://medium.com/@polo13999/mongo-dokcer-%E5%88%9D%E5%A7%8B%E8%A8%AD%E5%AE%9A-%E5%AD%B8%E7%BF%92%E6%89%8B%E9%9B%9C-bf3fd1b1178a)

```bash
mongo
use admin
db.createUser({ user: 'demo', pwd: 'demo123', roles: [ { role: 'userAdminAnyDatabase', db: 'admin' } ] });
# stop container
# remark command: mongod --auth
# start container
```

## nas

```bash
docker container ls
sudo docker exec -it 58553f890240 /bin/sh -c "[ -e /bin/bash ] && /bin/bash || /bin/sh"
```

## MongoDB Compass

- [MongoDB Compass](https://www.mongodb.com/download-center/compass)
- mongodb://demo:demo123@localhost:27017