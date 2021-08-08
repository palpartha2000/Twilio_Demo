# Sending message to a valid phone number using Twilio’s Programmable SMS Python application


### Prerequisite

* [Twilio account](https://www.twilio.com/try-twilio)
* Twilio phone number with SMS capabilities


## Part A - Send an SMS using the Programmable Twilio SMS API

1. Clone the repository to the development environment

2. In the send_sms.py

* Replace the placeholder values for **account_sid** and **auth_token** with your unique values. You can find these in your Twilio console

* Please note: it's okay to hardcode your credentials when getting started, but you should use [environment variables](https://www.twilio.com/blog/2017/01/how-to-set-environment-variables.html) to keep them secret before deploying to production. 

* Replace the __*from*__ number with the Twilio phone number you purchased earlier

* Replace the __*to*__ number with your mobile phone number
 
* We also include the __*body*__ parameter, which contains the content of the SMS we’re going to send.

###### For more reference https://www.twilio.com/docs/sms/tutorials/how-to-send-sms-messages-python#get-a-phone-number-with-sms-and-mms-capabilities



## Part B - Track Delivery Status of Messages in Python

1. To get Twilio to call your webhook, you need to provide a URL to your application in the __*status_callback*__ parameter of each message for which you want the status callbacks.

2. Now you need an URL which you can give to Twilio. Twilio can only access public servers on the Internet.

* You need to take your web application and publish it to a web or cloud hosting provider (of which there are many), or you can host it on your own server with public Web URL, or you can use a service such as ngrok <https://ngrok.com/docs> to expose your local development machine to the internet. 

* or Else you could also include a URL that points to your application by using a [RequestBin URL](https://requestbin.com/r/enp5ptt5jxpg/1wLgrDX257uIQUiKXG3dHmmehRf) instead, so that we can easily inspect the webhook requests that Twilio sends

###### For more reference https://www.twilio.com/docs/sms/tutorials/how-to-confirm-delivery-python#


#### Once you’ve updated the code sample, you can test it out by running it from the command line:
`python send_sms.py`

#### Output will appear as below in the terminal:

`SMS-id`
`queued`  -> This is the SMS status


*__This can also be viewed from http header as below:


`"SmsSid": "SMS-id"`
`"SmsStatus": "delivered"`
`"MessageStatus": "delivered"`
`"To": "+15558675310"`
`"MessageSid": "SMS-id"`
`"AccountSid": "Twilio-Account"`
`"From": "+15017122661"`
`"ApiVersion": "2010-04-01"`


