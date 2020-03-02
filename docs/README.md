# group_webscraper

IB CS group webscraper

## Documentation

For the Python Webscraper I contributed to the output function. This can be seen on lines `68-78` in `def output`. <br>

```python
def output(change_message, user_config):
          twilio_sid = user_config["twilio_sid"]
          twilio_auth = user_config["twilio_auth"]
          twilio_phone = user_config["twilio_phone"]
          user_phone = user_config["user_phone"]
          # print(twilio_sid, twilio_auth, twilio_phone, user_phone, message)
          client = Client(twilio_sid, twilio_auth)
          message = client.messages.create(
              body=change_message, from_=twilio_phone, to=user_phone
          )
          print(message.sid)
```

### My contributions

I set up the output function to accept the output from our magic happens function. This function takes two arguments, `change_message` for the message to be sent and `user_config` for the dictionary that contains the twilio and user information. These are then passed to the proprietary Twilio documentation.
