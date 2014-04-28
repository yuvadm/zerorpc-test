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

## Heroku

### Init

```bash
$ heroku create
Creating app-name-9999... done, stack is cedar
http://app-name-9999.herokuapp.com/ | git@heroku.com:app-name-9999.git
$ git push heroku master
```

### Run
```bash
$ zerorpc -j tcp://app-name-9999.herokuapp.com:4242 add_42 1

FAIL :(
```

Heroku doesn't like plain TCP sockets...
