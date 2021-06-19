# gmail-reader-api
This Code written in Nodejs can fetch Email from gmail from your account and It can print 
them on the terminal . You can modify few line to change the number of mail you want to print .

# To get started for using this API 
first download and extract this . Then move to this project folder.
Now in your terminal in the same folder where you have index.js file type the following 
command 


$ npm init
$ npm i googleapis cheerio mailparser js-base64 open express

Now to Go to google developers console in your project. Navigate to the credentials part.
In OAuth 2.0 Client IDs, you'll find a small download icon, download your credentials
file from there and add to your folder where you've created this project. Name this file as

credentials.json
I have show a sample file as credentials.json in my this repo but these credentials are dummy
credentials but your original credential file will look similar to credentials.json in this
repository .

Run your code in your terminal. You will get a URL printed on your console .
Click on that URL Now here comes the tricky part . If that website is opened then simply copy 
code but if it shows error cannot reach to the website .
Then click on address bar of your browser where that url is opened website will be something like 
localhost:3000/?code=4/0AY0e-g5EwrM0StlcVmOx00gudhhjkjkjhUmcCXQ7XEe1b7SOX-9e7bDfuAQ&scope=https://www.googleapis.com/auth/gmail.modify

Now you need to copy from code= to before '&' symbol . For example website we need to copy the
code which is below   
4/0AY0e-g5EwrM0StlcVmOx00gudhhjkjkjhUmcCXQ7XEe1b7SOX-9e7bDfuAQ
Delete token.json from your working directory if created .

Now run this file and You will see your email in terminals .

##  If you want to change  no. of emails to be printed on terminal
You need to modify function listMessages . In this function we call 
getMail(res.data.messages[0].id, auth) intstead you can change 0 to another value to see next email(here max value you 
can put is 5  Read further if you want to know more about it ) .
Note that do not read many emails at a time this may crash the app .
Also if you read this function listMessages in index.js you will see that there is one variable called "maxResults:5 "
Changing Max result to 6 or 8 or whatever you want then you can put corresponding no (or no-1 to be precise ) . 


