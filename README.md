# koa2-token

## Usage

```bash
# start server listen 3333
node app.js
```

```
$ curl http://127.0.0.1:3333/api/userInfo

Authentication Error%
```

```
$ curl -d "name=peng" http://127.0.0.1:3333/api/login

{"message":"获取token成功","code":1,"token":"eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJuYW1lIjoicGVuZyIsImlhdCI6MTU0MTk5NTYyMywiZXhwIjoxNTQxOTk5MjIzfQ.x3vhRuf4mDxBfbD-Uc74Sdc00X0qXwRmX6GFtSjDrYM"}%
```

```
$ curl -H "Authorization: Bearer eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJuYW1lIjoicGVuZyIsImlhdCI6MTU0MTk5NTYyMywiZXhwIjoxNTQxOTk5MjIzfQ.x3vhRuf4mDxBfbD-Uc74Sdc00X0qXwRmX6GFtSjDrYM" http://127.0.0.1:3333/api/userInfo

{"payload":{"name":"peng","iat":1541995623,"exp":1541999223}}%
```
