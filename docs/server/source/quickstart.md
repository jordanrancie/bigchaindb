# Quickstart

This page has instructions to set up a single stand-alone BigchainDB node for learning or experimenting. Instructions for other cases are [elsewhere](introduction.html). We will assume you're using Ubuntu 16.04 or similar. If you're not using Linux, then you might try [running BigchainDB with Docker](appendices/run-with-docker.html).

A. Install MongoDB as the database backend. (There are other options but you can ignore them for now.)

[Install MongoDB Server 3.4+](https://docs.mongodb.com/manual/tutorial/install-mongodb-on-ubuntu/)

B. Run MongoDB. Open a Terminal and run the command:
```text
$ sudo mongod --replSet=bigchain-rs
```

C. Ubuntu 16.04 already has Python 3.5, so you don't need to install it, but you do need to install some other things:
```text
$ sudo apt-get update
$ sudo apt-get install g++ python3-dev libffi-dev
```

D. Get the latest version of pip and setuptools:
```text
$ sudo apt-get install python3-pip
$ sudo pip3 install --upgrade pip setuptools
```

E. Install the `bigchaindb` Python package from PyPI:
```text
$ sudo pip3 install bigchaindb
```

F. Configure BigchainDB Server:
```text
$ bigchaindb -y configure mongodb
```

G. Run BigchainDB Server:
```text
$ bigchaindb start
```

You now have a running BigchainDB Server and can post transactions to it.
One way to do that is to use the BigchainDB Python Driver.

[Install the BigchainDB Python Driver (link)](https://docs.bigchaindb.com/projects/py-driver/en/latest/quickstart.html)

<hr>

<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
