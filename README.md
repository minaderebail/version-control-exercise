# version-control-exercise

## Setup

Create a new virtual environment (first time only):

```sh
conda create -n reports-env python=3.10
```

Activate the virtual environment (whenever you come back to this project): 

```sh
conda activate reports-env
```


Install packages:

```sh
pip install -r requirements.txt
```


[Obtain an API Key](https://www.alphavantage.co/support/#api-key) from AlphaVantage.

Email-sending functionality:
To use SendGrid for sending email, you must first follow some setup instructions to create an account, verify your account, setup a single sender address and verify it, then finally obtain an API Key:

First, sign up for a SendGrid account, and click the verification link sent to your email address. (https://signup.sendgrid.com/)

Then follow the instructions to complete your "Single Sender Verification", and click the verification link sent in another confirmation email to verify your single sender address (i.e. the SENDGRID_SENDER_ADDRESS). You should be able to access these settings via the "Sender Authentication" section of the settings menu.

Finally, create a SendGrid API Key with "full access" permissions (i.e. the SENDGRID_API_KEY). You should be able to access these settings via the "API Keys" section of the settings menu. (https://app.sendgrid.com/settings/api_keys)

NOTE: Sometimes SendGrid may deny your application for seemingly no reason. Try using your personal gmail address as the single sender, and put information related to your business or university (like the address) as the business information.

NOTE: If working in a group or development team, only one group member needs to get this set up successfully, and you can consider sharing credentials with other group members.

Once you have obtained the credentials, set them as env variables in the called SENDGRID_SENDER_ADDRESS and SENDGRID_API_KEY, respectively.

Create a ".env" file and add contents like the following (using your own AlphaVantage API Key):

```sh
# this is the ".env" file:
ALPHAVANTAGE_API_KEY="..."
SENDGRID_API_KEY="..."
SENDGRID_SENDER_ADDRESS="..."
```


## Usage

Run the example script:

```sh
python app/example.py
```


Run the unemployment report:

```sh
python app/unemployment_report.py
```


Run the stocks report:

```sh
python app/stocks_report.py
```


Run the example email sending file:

```sh
python app/email_service.py
```