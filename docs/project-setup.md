# Steps to Start the Project

## Setup VS Code to run python
1. Enable Python Extension for this workspace
2. Select python interpretor (`ctrl + p` => `enter > + select entrpreter` => choose from available interpretors).
[Read More from VS Code docs](https://code.visualstudio.com/docs/python/python-tutorial)

## Run the project
To run this application there are 2 steps required:
1. Initialize the database by using the `python init_db.py` command. This will create or overwrite the `database.db` file that is used by the web application.
2.  Run the TechTrends application by using the `python app.py` command. The application is running on port `3111` and you can access it by querying the `http://127.0.0.1:3111/` endpoint.