Flask-SocketIO
==============

[![Build status](https://github.com/miguelgrinberg/flask-socketio/workflows/build/badge.svg)](https://github.com/miguelgrinberg/Flask-SocketIO/actions) [![codecov](https://codecov.io/gh/miguelgrinberg/flask-socketio/branch/main/graph/badge.svg)](https://codecov.io/gh/miguelgrinberg/flask-socketio)

Socket.IO integration for Flask applications.

Sponsors
--------

The following organizations are funding this project:

![Socket.IO](https://images.opencollective.com/socketio/050e5eb/logo/64.png)<br>[Socket.IO](https://socket.io)  | [Add your company here!](https://github.com/sponsors/miguelgrinberg)|
-|-

Many individual sponsors also support this project through small ongoing contributions. Why not [join them](https://github.com/sponsors/miguelgrinberg)?

Installation.
------------

You can install this package as usual with pip:

    pip install flask-socketio

Example
-------

```py
from flask import Flask, render_template
from flask_socketio import SocketIO, emit
    
app = Flask(__name__)
app.config['SECRET_KEY'] = 'secret!'
socketio = SocketIO(app)

@app.route('/')
def index():
    return render_template('index.html')

@socketio.event
def my_event(message):
    emit('my response', {'data': 'got it!'})

if __name__ == '__main__':
    socketio.run(app)
```

Resources
---------

- [Tutorial](http://blog.miguelgrinberg.com/post/easy-websockets-with-flask-and-gevent)
- [Documentation](http://flask-socketio.readthedocs.io/en/latest/)
- [PyPI](https://pypi.python.org/pypi/Flask-SocketIO)
- [Change Log](https://github.com/miguelgrinberg/Flask-SocketIO/blob/main/CHANGES.md)
- Questions? See the [questions](https://stackoverflow.com/questions/tagged/flask-socketio) others have asked on Stack Overflow, or [ask](https://stackoverflow.com/questions/ask?tags=python+flask-socketio+python-socketio) your own question.

