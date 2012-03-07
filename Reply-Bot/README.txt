This python script is a basic repeat twitter bot written by Heat Miser (heatmiser.contact@gmail.com).


Prerequisites for using this bot
================================

This script has been tested with Python 2.7.

A few libraries are mandatory to use the script:

- ConfigParser: used to parse the config file
  	You can use "easy_install" command to instal it easily (ex: sudo easy_install ConfigParser) or download it directly at http://docs.python.org/library/configparser.html

- tweepy: used to manage the Twitter's API calls
  	If available on your system you can use "easy_install" too (ex: sudo easy_install tweepy) or download it at http://code.google.com/p/tweepy/

- sqlite3: used to save credentials and statuses id.
  	 This library should be available with your python version. If necessary you can try an install with "easy_install".


Twitter API and Consumer Key
============================

In order to use the script you must register your application to have an API Consumer Key and Secret. These are mandatory to use the API.

You can register your application after authentication here : https://dev.twitter.com/apps/new


How to set up the config file
=============================

Many fields of the "bot_config.ini" file must be filled before lauching the bot for the first time.

Precisions about the file format:
- the separator for the concerned fields is just a " " (standard space)
- each field must be filled in a single line (no newline)

Fields descriptions:
- CONSUMER_KEY and CONSUMER_SECRET: key and secret provided by Twitter after app registration

- DATABASE_PATH: relative or absolute path to the sqlite file used by the app

- LOGFILE_PATH: relative or absolute path to the log file used by the app

- LOG_LEVEL: verbosity level for the loggin mechanism. Values can be DEBUG INFO WARNING ERROR CRITICAL 

- BOTNAME: the bot screen name 

- NOREPLY_ACCOUNTS: a list (space separated) of twitter accounts the bot must ignore

- MESSAGE: the replied tweet (must be less than 140 char (don't forget the reply login). 130 char is a good max length.

- KEYWORDS: the search expression used to match the tweets which must be replied. You can elaborate your search expression on the official Twitter search engine: http://search.twitter.com

- SLEEP_TIME: the sleep time in seconds between each execution (must be an int value). 90 is a good value.

Misc.
=====

The script is not daemonized, I recommend you to run it into a "screen" session in order to ensure bot availability. 
