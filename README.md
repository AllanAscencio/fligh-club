# Flight Club

Flight Search App

Automated self messaging app to never miss the cheapest flights to the destination of your choosing.

This application is installable locally in desktop.

## Built With

- Python

## Getting Started

To get a local copy up and running follow these simple example steps.

### Setup

- Open the console
- Download or git clone https://github.com/AllanAscencio/flight-club
- cd flight-club
- Create your account on https://sheety.co/ in order to get your free API, to see their documentation you must first create a new project in which you must provide the link of your google sheet excel. Once that is done you can enter you project and read the tab where is says API and you are going to have everything you need.
- Create your account on https://tequila.kiwi.com/portal/login to acquire your free API. After you created your account you can access the documentation https://tequila.kiwi.com/portal/getting-started and to receive an API key you must first 'create a solution' in which you can select the parameters of your choosing for what you are going to use the API.
- Create your account on https://www.twilio.com/ in order to get your free API and AUTH, to see their documentation visit https://www.twilio.com/docs/sms

Install requests:

Linux

```
  $ pip install requests 
```

In Linux, If you require root permission, use ‘sudo’. Alternatively, you can also use pipenv to install requests library, where pipenv is used to automatically manage the packages during the course of installation/uninstallation.

```
$ pip install pipenv
```

Windows

The Windows users need to navigate to the Python directory, and then install the request module as follows:

```
> python -m pip install requests
```

Mac
For MacOS, install Python through ‘Home Brew’. Thereafter, install pip and request module (which is the same as Linux installation process.)

Install twilio:

The easiest way to install the library is from PyPi using pip, a package manager for Python. Simply run this in a terminal:

```
pip3 install twilio
```
If you get a pip: command not found error, you can also use easy_install. Run this in your terminal:

```
easy_install twilio
```
Manual twilio installation

Alternatively, you can download the source code (ZIP) for twilio-python https://github.com/twilio/twilio-python/zipball/main, and then install the library by running: 
```
python3 setup.py install
```
in the folder containing the twilio-python library.

“Permission Denied”
If the command line gives you a big long error message that says Permission Denied in the middle of it, try running the above commands with sudo (e.g., sudo pip3 install twilio).

### Test your installation

Try sending yourself an SMS message. Save the following code sample to your computer with a text editor. Be sure to update the account_sid, auth_token, and from_ phone number with values from your Twilio account. The to phone number can be your own mobile phone.
```
from twilio.rest import Client

# Your Account SID from twilio.com/console
account_sid = "ACXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX"
# Your Auth Token from twilio.com/console
auth_token  = "your_auth_token"

client = Client(account_sid, auth_token)

message = client.messages.create(
    to="+15558675309", 
    from_="+15017250604",
    body="Hello from Python!")

print(message.sid)
```

Author
👤 **Allan Ascencio**

- [Github](https://github.com/AllanAscencio)
- [Linkedin](https://www.linkedin.com/in/gianfranco-allan)


## Considerations

- The default city of origin I selected for testing this project is London, which is in the main.py file. You may change it to the city that sits you best. but REMEMBER that it MUST BE in IATA coding. This is very important.
- Becaue the city I selected is London, the currency is also in pounds, so you may also change that in the flight_search.py file, in the check_flights function you can change the currency  which is typed as "curr": "GBP" and on flight_data = FlightData you can change the currency sign from £ to the one you prefer.

## 🤝 Contributing

Contributions, issues and feature requests are welcome!

## Show your support

Give a ⭐️ if you like this project!

## 📝 License

This project is [MIT](https://opensource.org/licenses/MIT) licensed.
