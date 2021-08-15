## Deploying slam-mirrorbot on Heroku with Github Workflows.

## Pre-requisites

- [Heroku](heroku.com) accounts
- Recommended to use 1 App in 1 Heroku accounts
- Don't use bin/fake credits card, because your Heroku account will banned

## Deployment

1. Give stars and Fork this repo then upload **token.pickle** to your forks, or you can upload your **token.pickle** to your Index and put your **token.pickle** link to **TOKEN_PICKLE_URL** (**NOTE**: If you didn't upload **token.pickle** uploading will not work). How to generate **token.pickle**? [Read here](https://github.com/breakdowns/slam-mirrorbot#getting-google-oauth-api-credential-file)

2. Go to Repository `Settings` -> `Secrets`

	![secrets](https://telegra.ph/file/bb8cb0eced5caad68a41b.jpg)

3. Add the below Required Variables one by one by clicking `New Repository Secret` everytime.

	```
	HEROKU_EMAIL
	HEROKU_API_KEY
	HEROKU_APP_NAME
	```

	### Description of the above Required Variables
	* `HEROKU_EMAIL` Heroku Account email Id in which the above app will be deployed
	* `HEROKU_API_KEY` Go to your Heroku account and go to Account Settings. Scroll to the bottom until you see API Key. Copy this key and add it
	* `HEROKU_APP_NAME` Your Heroku app name, Name Must be unique

4. [Setting up config file](https://github.com/breakdowns/slam-mirrorbot#setting-up-config-file)
	* Rename `config_sample.env` to `config.env`
	* Remove the first two lines of the file
	![Remove Line](https://telegra.ph/file/44202b627479d4f237f7c.jpg)
	* Fill Required Config from [Here](https://github.com/breakdowns/slam-mirrorbot/blob/master/config_sample.env) (**NOTE**: You also can fill optional config)

5. After adding all the above Required Variables & Required Config go to Github Actions tab in your repo

6. Select `Manually Deploy to heroku` workflow as shown below:

	![Example Manually Deploy to Heroku](https://telegra.ph/file/38ffda0165d9671f1d5dc.jpg)

7. Then click on Run workflow

	![Run workflow](https://telegra.ph/file/c5b4c2e02f585cb59fe5c.jpg)

8. _Done!_ your bot will be deployed now.

## NOTE
- Don't change/edit variables from Heroku if you want to change/edit do it from Github Secrets
- If you want to set optional variables, go to your Heroku app settings and add the variables

## Credits
- [arghyac35](https://github.com/arghyac35) for Tutorial
