# fun3w/mongodb

- [30-2之使用Docker來建構MongoDB環境](https://ithelp.ithome.com.tw/articles/10184657)
- [Dokcer Mongo 初始化權限設定 學習手雜](https://medium.com/@polo13999/mongo-dokcer-%E5%88%9D%E5%A7%8B%E8%A8%AD%E5%AE%9A-%E5%AD%B8%E7%BF%92%E6%89%8B%E9%9B%9C-bf3fd1b1178a)

```bash
mongo
db.createUser({ user: 'demo', pwd: 'demo123', roles: [ { role: 'userAdminAnyDatabase', db: 'admin' } ] });
# stop container
# remark command: mongod --auth
# start container
mongo -port 27017 -u 'myUserAdmin' -p 'abc123' -authenticationDatabase 'admin'


use admin
db.createUser({
  user: 'root',
  pwd: 'root',
  roles: [{role: 'userAdminAnyDatabase', db: 'admin'}]
})


use test
db.createUser({
  user: 'test',
  pwd: 'test',
  roles: [{role: 'readWrite', db: 'test'}]
})
```