GroupMe Data Collection
--------------

Originally written by Abu Qader
Updated to Python 3.6 by Matt Dalton
This is a set of simple scripts to download data from GroupMe's API for a particular chat. It ouputs everything into a CSV file and can be used to look at user analytics, group analytics and even some interesting ML applications. 

Requirements:
--------------
In order to use this, GroupMe will have to supply an API token to grant access to their API. To get this, log into GroupMe's <a href="https://dev.groupme.com/session/new" target="_blank">Developers</a> website and click Access Token on the upper right.

Instructions
--------------
1. Get your GroupMe Access Token using the instructions above.
2. Run ```python retrieve_msgs.py```, pass in your access token, and follow the command line interface to download your GroupMe messages to a CSV file. Use ```python retrieve_msgs.py --help``` to see a list of commands. Below are some sample usages:
  - ```python retrieve_msgs.py <YOUR ACCESS TOKEN> -a -c output.csv``` will output all of your GROUP messages into a csv file called output.csv.
  - ```python retrieve_msgs.py <YOUR ACCESS TOKEN> -g "Random Group Name"``` will get data for your group into a CSV file named after the group
  - ```python retrieve_msgs.py <YOUR ACCESS TOKEN> -d -a``` will output all of your DIRECT MESSAGES into a separate csv file for each person.
  - ```python retrieve_msgs.py <YOUR ACCESS TOKEN> -d -g "Random Person" -c jlaw.csv``` will output your DIRECT MESSAGES from that person into a csv file. 
  
Adapted from @youyanggu for 3.6

