## New style of Handler

*now you only pass a decorator for hook any functions which you want*


# Example
```python

from mains import MainBots

init = MainBots(token="YOUR TOKEN")

@init.poll.message_handler(type=26)
def receive_message(client, message):
    """
    type: class <int>
    client: class <linepy.client.LINE>
    message: class <akad.ttypes.Message>
    
    what's meant?
    type of type must classes from int
    type 26 that's meant OpType.RECEIVE_MESSAGE
    
    :Return: client object and Message objects
    """
    pass
    
#Run bot
init.runs()
```

## Any example for any Notified

```python

@init.poll.message_handler(type=19)
def notif_kicked(client, message):
    pass

@init.poll.message_handler(type=13)
def notif_joined(client, message):
    pass
    
@init.poll.message_handler(type=32)
def notif_cancled(client, message):
    pass
```
> TODO: i'll update features as soon as possible, if you and any idea or found some bug free for report
