# Truecaller/Smsbomber-telegram_bot

Add your telegram bot api key in main.py and you are good to go

To get a api key Goto telegram and search BotFather 

From the commands select /newbot and give it a name and you're done

Now added webhook to make the bot little bit faster if it has more traffic

To use webhook version 

1. Create a webhook with link below

    https://api.telegram.org/bot{ your api key }/setwebhook?url=https://{ your heroku app name }.herokuapp.com
    

2.when you see webhook was set message when you open the link then you succesfully setup the webhook

3.Go to main_webhook.py and add your api key at line 13 and your heroku app name at line 76



4.To make it run on heroku without webhook the Procfile should be 

     worker: python main.py

5.To use webhook version change your Procfile to

     web: python main_webhook.py 

6.Then type this command in your heroku cli if you encounter any error in logs(only for webhook version)

     heroku ps:scale web=1 -a your_heroku_app_name
