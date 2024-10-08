# Auto-Filter-Bot-Public

## Features ✅
- Unlimited filter adding.
- Support Telegram Buttons and Alerts.
- Anyone can add filters after connecting their chats
- When a group connection is deleted all the filters related to that group also get deleted to save database storage.
- Disconnected chats can be connected again if needed. All the previous filters works for the connected group.

## Installation

### Deploy in your vps
#### We are gonna use docker compose to run the bot.
Install docker on your VPS. See official [Docker Docs.](https://docs.docker.com/engine/install/ubuntu/)
<br> After installing docker follow the below steps.</br>
1. Clone the repo and change directory to Auto-Filter-Bot
```
git clone https://github.com/pachax001/Auto-Filter-Bot.git && cd Auto-Filter-Bot/
```
2.Rename sample_config.env to config.env and fill config.env
```
cp sample_config.env config.env
```
Edit config.env
```
nano config.env
```
3. After filling and saving config.env type this command in terminal and press enter.
 ```
sudo docker compose up
```
### Extra

1. To stop docker container
 ```
sudo docker compose down
```
2. To delete stopped containers.
```
sudo docker system prune -a
```

## Configs
### config.env file

- `APP_ID`        - From my.telegram.org (or @UseTGXBot)

- `API_HASH`      - From my.telegram.org (or @UseTGXBot)

- `TG_BOT_TOKEN` - Get it from @BotFather
-  `DATABASE_URI`- MongoDB URL ([Click here](https://github.com/pachax001/Auto-Filter-Bot/blob/main/README.md#-generate-mongodb-database) for more info on MongoDB URL.)
-  `DATABASE_NAME` - MongoDB Cluster name (Default is `Cluster0`)
-  `AUTH_USERS` - Authorized Users. Doesn't do anything. Keep it blank. But need for private version.
-  `OWNER_ID` - Owner ID of the bot owner. Get it from @MissRose_bot
-  `SAVE_USER` - Save the users who have start the bot. Values are `YES` or `NO`. Will take the space from database.
-  `ADD_FILTER_CMD` - Custom command for filter adding. Default is `add`.
-  `DELETE_FILTER_CMD` - Custom command for deleting filters. Default is `del`.
-  `DELETE_ALL_CMD` - Custom command for deleting all filters of the connected chat. Default is `delall`.
-  `CONNECT_COMMAND`- Custom command for connecting to chat. Default is `connect`.
-  `DISCONNECT_COMMAND` - Custom command for disconnecting from the curerntly connected chat. Default is `disconnect`.
- `CONNECTIONS_COMMAND` - To view connections. Default is `connections.`
-  `VIEW_FILTERS_COMMAND` - To view all filters of the currently connected chat. Default is `filters`.


### 🤖 ***Bot Commands (Default)***
```
start - Start the bot
connect - Connect to a chat
disconnect - Disconnect from a chat
connections - To see all the connections
del - Delete filters
delall - delete all filters of the currently connected chat
filters - To view all filters of the currently connected chat
help - Get details about how to use bot
about - About the bot
```
### 📡 ***Generate MongoDB Database***

1. Go to `https://mongodb.com/` and sign-up.
2. Create Shared Cluster.
3. Press on `Database` under `Deployment` Header, your created cluster will be there.
5. Press on connect, choose `Allow Acces From Anywhere` and press on `Add IP Address` without editing the ip, then create user.
6. After creating user press on `Choose a connection`, then press on `Connect your application`. Choose `Driver` **python** and `version` **3.12 or later**.
7. Copy your `connection string` and replace `<password>` with the password of your user, then press close.

## 🏅 **Credits**
|<img width="70" src="https://avatars.githubusercontent.com/u/88532565">| <img width="70" src="https://avatars.githubusercontent.com/u/70193223">|

|[`Pyrofork`](https://github.com/Mayuri-Chan/pyrofork)|[`Base Repo`](https://github.com/TroJanzHEX/Unlimited-Filter-Bot)|

