### flower
---
https://github.com/mher/flower

```sh
curl -X POST http://localhost:5555/api/worker/pool/restart/myworker
curl -X POST -d '{"args":[1,2]}' http://localhost:5555/api/task/async-apply/tasks.add
curl -X POST -d 'terminate=True' http://localhost:5555/task/revoke/xxxx

pip install flower
pip install https://github.com/mher/flower/zipball/master

flower --port=5555
celery flower -A proj --address=127.0.0.1 --port=5555
celery flower -A proj --broker=amqp://guest:guest@localhost:5672//
flower --unix_socket=/tmp/flower.sock
```

```py
var ws = new WebSocket('ws://localhost:5555/api/task/events/task-succeeded/');
ws.onmessage = function (event) {
  console.log(event.data);
}
```

```
```


