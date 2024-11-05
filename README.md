# How to

Once you have the script in your local folder, create a symbolic link to the `/usr/local/bin` folder like this:


```sh
# provide execution permissions
chmod +x aws-sso-login-profile
# Make the softlink
ln -s $(echo $PWD)/aws-sso-login-profile /usr/local/bin/.
```
prompts the `zsh` terminal to start a new interpreter session, or starts a new terminal.

### In Example:

```sh
laptop[~]$ aws-sso-login-profile

Listing AWS-SSO Profiles:

     1  account-dev
     2  account-prod
     3  account-support

Select the profile you want to access [1..3]: 1

SSO-Login to: account-dev


Attempting to automatically open the SSO authorization page in your default browser.
If the browser does not open or you wish to use a different device to authorize this request, open the following URL:

https://device.sso.<REGION>.amazonaws.com/

Then enter the code:

XXXX-XXXX
Successfully logged into Start URL: https://<URL>
laptop[~]$ 
```

