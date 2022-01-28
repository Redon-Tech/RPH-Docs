---
authors:
    - parker02311
---
## Requirements

- A computer or VPS to host the bot/api on
    - Make sure it has an open port for the API to run on
    - Note: Glitch will not work for this as it must be online 24/7.
- Have a database setup on [MongoDB](https://www.mongodb.com/)
- Have a [Discord bot](https://discord.com/developers) setup and the token ready.
- Have a Roblox cookie ready. (Toturial on how to get soon)
- Python 3.9 Installed(With pip)
- Git installed for fast setup

## Database Setup

1. Create a cluster called `data`
    - Have a database called `users` and `products` created under the cluster
2. Setup the database user and make sure to remember the password you will need it later
3. Hit the connect button and allow connections from everyone `0.0.0.0/0`
4. When prompted with a screen to chose a connection method click on use mongos native drivers
5. Change the programming language to python and copy the URL and save it for later