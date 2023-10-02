# easy-apply-bot
### A LinkedIn Easy Apply bot to help with my job search.

Getting Started
------------
First, clone the repository somewhere onto your computer, or download the .zip, extract, and navigate into the folder.
Assuming you have Python3 installed, activate a virtual environment (optional) and enter the following command.

`pip3 install -r requirements.txt`

The config file template is shown below. 
You'll need to edit this according to what jobs you are looking for, and their locations. 
You will also need to add in your LinkedIn credentials. 
Only Easy Apply postings will be selected.
Set "experience" from 1-6 to refine search to your experience level: intern/entry level/associate/mid-senior level/director/executive.
Make sure that the config file follows proper json syntax.

```
{
    "username": "username",
    "password": "password",
    "job_titles": [
        "Software Engineer",
        "Developer"        
    ],
    "locations": [
        "Canada",
        "Remote"
    ],
    "experience": 2
}
```

A sqlite3 database will save the job title, company, location, workplace type, and the url of the LinkedIn posting that you have applied to.

`python3 easy-apply.py` in the project directory should run the bot.
