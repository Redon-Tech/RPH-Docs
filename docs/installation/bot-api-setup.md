## Installation
1. Clone this repository into the directory you want it in.
    
    Via Git:
    ```shell
    git clone https://github.com/Redon-Tech/Roblox-Purchasing-Hub
    ```
    Via Get(Development Version):
    ```shell
    git clone -b development https://github.com/Redon-Tech/Roblox-Purchasing-Hub
    ```
2. Install requirements
    ```shell
    cd Roblox-Purchasing-Hub

    pip3 install -r BOT/requirements.txt
    ```
    If that isnt working do
    ```shell
    pip install -r BOT/requirements.txt
    ```
3. In BOT/lib/bot clone the example.config.json and rename it to config.json
4. Edit config.json and update it with all the proper information (Guide on configuration below)
5. In BOT/lib/cogs/website.py at the very bottom change
    ```python
    app.run_task("0.0.0.0")
    ```
    To (Replace 5000 with your open port)
    ```python
    app.run_task("0.0.0.0", port=5000)
    ```
6. Run the bot by executing BOT/launcher.py
    ```shell
    python3 BOT/launcher.py
    ```
    If that isnt working do
    ```shell
    python BOT/launcher.py
    ```
7. Test that the bot is online by using `{prefix}help` (Default Prefix: ".")

## Configuration
```json
{
    "token": "",
    "prefix": ".",
    "ownerids": [
        1234567890
    ],
    "guild": 1234567890,
    "standardoutput": 123467890,
    "usepages": true,
    "mongodb": {
        "url": "mongodburl"
    },
    "roblox": {
        "cookie": "fullrobloxcookie"
    },
    "apikey": "generatearandomstringforthis"
}
```

- Token [String]: The token of your bot found at [Discord Developer Portal](https://discord.com/developers).
- Prefix [String]: The prefix of the bot. [Default: "."]
- OwnerIds [List of Numbers]: List of all the bot owners, used for owner commands.
- Guild: [Number]: The primary guild id of the bot. Also the guild that the standard output channel is in.
- StandardOutpu [Number]: The output channel id for bot logs.
- UsePages [Bool]: N/A
- MongoDB [Dictionary]: All information for MongoDB
- MongoDB.URL [String]: The connection URL to your [MongoDB](https://www.mongodb.com/) server.
- Roblox [Dictionary]: All information for Roblox
- Roblox.Cookie [String]: The full Roblox cookie of your Roblox bot.
- ApiKey [String]: Should be a random string used for communication between API and database.
