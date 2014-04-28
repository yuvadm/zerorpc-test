# ZeroRPC Test

A simple test to get ZeroRPC for Python running on Heroku.

## Local Dev

### Server

```bash
$ python server.py
```

### Client
```bash
$ zerorpc -j tcp://localhost:4242 add_42 1
43
$ zerorpc tcp://localhost:4242 add_man 'I own a mint-condition Volkswagen Golf'
"I own a mint-condition Volkswagen Golf, man!"
$ zerorpc tcp://localhost:4242 boat 'I own a mint-condition Volkswagen Golf, man!'
"I'm on a boat!"
```
