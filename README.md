# Honeygain Bot
Honeygain Bot opens the honey jar for you without even going on their website. You can login via your access token or your email and password. You can configure the bot to open the honey jar at 00:00 GMT or just once before it shuts itself down. The reason it opens at 00:00 GMT is because that is when the Honeygain server resets. You can set this up on a server and leave it running for as long as you want, I will be running this on a Raspberry PI.

## Warning
I have contacted someone at Honeygain about this bot, they've informed me to use this program at my own risk. I would not recommend using this bot with your login info, as you can get your account suspended if you use your email and password with this bot too much, access token is preferred. Before using this program, make sure you would be ok with your account getting suspended. Do not hold me accountable for any account bans/suspensions.

## Access Token
An access token is a string of letters that is used to perform actions on your account. To get your access token, open developer tools (or inspect element) on a chromium based browser and go to the console tab. Type in `localStorage.getItem('JWT')` into the console and press enter. The console with print your access token.

## Installation
Make sure the device you're running this on syncs its time to the internet automatically.
If you want to login with your email and password, edit the run_login.bat file. Enter your email at the end of `set email=` and enter your password at the end of `set password=`. Now you can double click the run_login.bat file.

If you want to login with your access token, edit the run_token.bat file. Simply enter your access token (with or without the quotation marks on either end) at the end of `set access_token=`. Now you can double click the run_token.bat file.

If you don't want to use the .bat files, you can manually execute the bot with terminal/cmd:

    java -jar HoneygainBot.jar [Access Token] [Repeat everyday? True/False]

 For email and password:

    java -jar HoneygainBot.jar [Email] [Password] [Repeat everyday? True/False]

## Update (4/20/22)
    
    This still works but now you have to be an active earner or the API won't let you claim
