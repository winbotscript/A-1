# ![Logo](https://github.com/dyseo/X/blob/master/examples/assets/LINE-sm.png) Line-A
_Bot line with Private Message's API_

[![python3.x](https://img.shields.io/badge/python-3.x-green.svg)](https://www.python.org/downloads/release/python-372/) [![License](https://img.shields.io/badge/MIT-License-blue.svg)](https://opensource.org/licenses/MIT) ![Version](https://img.shields.io/badge/Version-0.3-red.svg) ![Travis](https://travis-ci.org/dyseo/A.svg?branch=master)



### Simplify wrapper Unofficial Bot Python using Library from [Linepy](https://pypi.org/project/linepy/3.0.8/)

## Features
- [x] Including MultiThread
- [x] Simply login
- [x] More than fasted
- [x] Included simple Decorator

## Installing Linepy
* install [Linepy](https://pypi.org/project/linepy/3.0.8/) from [Pypi](pypi.org) not necessary
 
     `pip3 install linepy`

* install requirements attached

     `pip3 install -r requirements.txt`
     
## How to use bot  
```python
from mains import MainBots
from linepy import OpType

init = MainBots(token="YOUR TOKEN HERE")
"""
declarate this line for your Bots
you can use email and password for login into bot
init = MainBots(email='your email', passwd='your mail password')
or you can pass args for getting QRCode URL
init = MainBots()
"""

def receive_message(client, operations):
    """
    use this method to implement your bot if Message income from user
    client = :Classes: <linepy.client.LINE object>
    this mean for used any functions from clinet e.g: client.sendMessage(..
    
    operation = :Classes: :Tuple: which contains a collection of messages
    e.g: Operations(revision=1, createdTime=1553146515644, type=25, reqSeq=994, checksum=None, status=None, param1='0', param2=None, param3=None, message=Message( ...
"""
message_handler = {
    OpType.RECEIVE_MESSAGE: receive_message
}
"""
pass message_handler Variable for your function without ()
you can use number from OpType for key of message_handler
e.g: message_handler = {26: receive_message} 26 meant same as OpType.RECEIVE_MESSAGE
"""

init.run(handler=message_handler)
#run BOT
```

> Look This [Example](https://github.com/dyseo/A/blob/master/bots) for more detail

## Run your bot
```bash
$ cd A
$ cd bots
$ python3 bot.py
```



# Author
[Line](line.me/ti/p/~line.bngsad) | [Telegram](t.me/alnyz)

## Thanks to:
Fadhiil Rachman / [Linepy](https://github.com/fadhiilrachman/line-py)



> ### TODO: if you have any idea or found some little bug or something, free for report to Author
