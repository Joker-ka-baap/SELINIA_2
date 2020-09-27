![Harita](https://telegra.ph/file/bfc6d21b24e9af9c79a62.png)
# Harita Robot 
[![Codacy Badge](https://api.codacy.com/project/badge/Grade/43872978473d46a0a44de96c96e62e27)](https://app.codacy.com/manual/Avishekbhattacharjee/Anie-Robot?utm_source=github.com&utm_medium=referral&utm_content=Avishekbhattacharjee/Anie-Robot&utm_campaign=Badge_Grade_Dashboard) 
[![made-with-python](https://img.shields.io/badge/Made%20with-Python-1f425f.svg)](https://www.python.org/)
[![Open Source Love svg2](https://badges.frapsoft.com/os/v2/open-source.svg?v=103)](https://github.com/ellerbrock/open-source-badges/) [![PRs Welcome](https://img.shields.io/badge/PRs-welcome-brightgreen.svg?style=flat-square)](http://makeapullrequest.com) [![Bot API Version](https://img.shields.io/badge/Bot%20API-v4.8-f36caf.svg?style=flat-square)](https://core.telegram.org/bots/api) [![Community Chat](https://img.shields.io/badge/Community-Chat-blueChat?style=flat-square&logo=telegram)](https://t.me/Haritasupport)
[![Telegram Channel](https://img.shields.io/badge/Telegram-Channel-orange)](https://t.me/HaritaNews)

A modular Telegram Python bot running on python3 with a sqlalchemy database. This is the Most Powerful Telegram Bot. You Can Clone The Bot At Your Own Risks.

Can be found on telegram as [Harita Robot](https://t.me/HaritaRobot).

The Support group can be reached out to at [Support](https://t.me/HaritaSupport), where you can ask for help about [Harita Robot](https://t.me/HaritaRobot), discover/request new features, report bugs, and stay in the loop whenever a new update is available. 

# Deploy The 100% Bugs Free Bot

Deploy it after editing main.py on tg_bot section. Don't join support group for folk support.




[![Deploy](https://www.herokucdn.com/deploy/button.svg)](https://heroku.com/deploy?template=https://github.com/Avishekbhattacharjee/Harita-Robot)

### Configuration

 
The following env variables are supported:

 - `bot_token`: Your bot token, as a string.
 - `owner_id`: An integer of consisting of your owner ID
 - `owner_username`: Your username
 - `api_key`: get it from my.telegram.org 
 - `api_hash`: get it from my.telegram.org
 - `database_url`: Your database URL
 - `message_dump`: optional: a chat where your replied saved messages are stored, to stop people deleting their old 
 - `load`: Space separated list of modules you would like to load
 - `no_load`: Space separated list of modules you would like NOT to load
 - `webhook`: Setting this to ANYTHING will enable webhooks when in env mode
 messages
 - `url`: The URL your webhook should connect to (only needed for webhook mode)

 - `sudo_users`: A space separated list of user_ids which should be considered sudo users
 - `whitelist_users`: A space separated list of user_ids which should be considered support users (can gban/ungban,
 nothing else)
 - `support_users`: A space separated list of user_ids, they can be banned.
 - `cert_path`: Path to your webhook certifdev_usersicate
 - `port`: Port to use for your webhooks
 - `del_cmds`: Whether to delete commands from users which don't have rights to use that command
 - `strict_gban`: Enforce gbans across new groups as well as old groups. When a gbanned user talks, he will be banned.
 - `strict_gmute`: Enforce gbans across new groups as well as old groups. When a gbanned user talks, he will be banned.
 - `workers`: Number of threads to use. 8 is the recommended (and default) amount, but your experience may vary.
 __Note__ that going crazy with more threads wont necessarily speed up your bot, given the large amount of sql data 
 accesses, and the way python asynchronous calls work.
 - `ban_sticker`: Which sticker to use when banning people.
 - `allow_excl`: Whether to allow using exclamation marks ! for commands as well as /.

### Python dependencies

Install the necessary python dependencies by moving to the project directory and running:

`pip3 install -r requirements.txt`.

This will install all necessary python packages.

### Database

If you wish to use a database-dependent module (eg: locks, notes, userinfo, users, filters, welcomes),
you'll need to have a database installed on your system. I use postgres, so I recommend using it for optimal compatibility.

In the case of postgres, this is how you would set up a the database on a debian/ubuntu system. Other distributions may vary.

- install postgresql:

`sudo apt-get update && sudo apt-get install postgresql`

- change to the postgres user:

`sudo su - postgres`

- create a new database user (change YOUR_USER appropriately):

`createuser -P -s -e YOUR_USER`

This will be followed by you needing to input your password.

- create a new database table:

`createdb -O YOUR_USER YOUR_DB_NAME`

Change YOUR_USER and YOUR_DB_NAME appropriately.

- finally:

`psql YOUR_DB_NAME -h YOUR_HOST YOUR_USER`

This will allow you to connect to your database via your terminal.
By default, YOUR_HOST should be 0.0.0.0:5432.

You should now be able to build your database URI. This will be:

`sqldbtype://username:pw@hostname:port/db_name`

Replace sqldbtype with whichever db youre using (eg postgres, mysql, sqllite, etc)
repeat for your username, password, hostname (localhost?), port (5432?), and db name.
