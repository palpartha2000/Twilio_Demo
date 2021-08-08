# Sending message to a valid phone number using Twilio’s Programmable SMS Python application


### Prerequisite

* [Twilio account](https://www.twilio.com/try-twilio)
* Twilio phone number with SMS capabilities



## Send an SMS using the Programmable SMS API

1. Clone the repository to the development environmnet

2. In the send_sms.py

..* Replace the placeholder values for **account_sid** and **auth_token** with your unique values. You can find these in your Twilio console

..* Please note: it's okay to hardcode your credentials when getting started, but you should use [environment variables](https://www.twilio.com/blog/2017/01/how-to-set-environment-variables.html) to keep them secret before deploying to production. 

..* Replace the __*from*__ number with the Twilio phone number you purchased earlier

..* Replace the __*to*__ number with your mobile phone number
 
..* We also include the __*body*__ parameter, which contains the content of the SMS we’re going to send.

###### For more reference https://www.twilio.com/docs/sms/tutorials/how-to-send-sms-messages-python#get-a-phone-number-with-sms-and-mms-capabilities



## Track Delivery Status of Messages in Python

1. To get Twilio to call your webhook, you need to provide a URL to your application in the __*status_callback*__ parameter of each message for which you want the status callbacks.

2. Now you need a URL you can give to Twilio. Twilio can only access public servers on the Internet.

..* You need to take your web application and publish it to a web or cloud hosting provider (of which there are many), you can host it on your own server, or you can use a service such as ngrok <https://ngrok.com/docs> to expose your local development machine to the internet. 

..* Else you would include a URL that points to your application by using a [RequestBin URL](https://requestbin.com/r/enp5ptt5jxpg/1wLgrDX257uIQUiKXG3dHmmehRf) instead, so that we can easily inspect the webhook requests that Twilio sends

###### For more reference https://www.twilio.com/docs/sms/tutorials/how-to-confirm-delivery-python#


#### Once you’ve updated the code sample, you can test it out by running it from the command line:
*__python send_sms.py__*









