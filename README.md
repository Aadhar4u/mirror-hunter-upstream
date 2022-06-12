#  UPSTREAM_REPO.

This is a modified repo of [arata74's MIRROR-HUNTER](https://github.com/arata74/MIRROR-HUNTER) & uses [anasty17's mltb](https://github.com/anasty17/mirror-leech-telegram-bot/tree/heroku) 'heroku' branch for bypassing ban.

![MIRROR HUNTER](https://media.giphy.com/media/dikubVwoUUBxLgpraV/giphy.gif?cid=790b7611c1fd9acab35e7fc75f7447316865d93043fc77b3&rid=giphy.gif&ct=s)

# Features & Fixes:

## ALL FEATURES OF [MLTB](https://github.com/anasty17/mirror-leech-telegram-bot) & [MIRROR-HUNTER](https://github.com/arata74/MIRROR-HUNTER)

## By [Maverick](https://telegram.dog/Maverick9099):
- Direct Clone from 
  > GDToT, AppDrive, DriveApp, DriveLinks, DriveAce, DriveBit, DriveSharer, DrivePro, GDFlix, HubDrive, KatDrive, DriveHub, Kolop, DriveFire, DriveBuzz and Sharer.pw links
- Fixed PyrogramEngine Errors!
- Fixed Last Summary Message of Leech (Now it goes to Leech Log Channel instead of Mirror Log Channel)
- Fixed MEGA (Earlier it was conflicting)
- Many more compatibility fixes !

### Note:
I am not the owner of these scrapers or codes. The credit goes to the developers who developed these scripts & codes.
I did some fixes on bot code and made some changes in these scrapers for bypassing more google drive sharers and fixed some issues regarding the compatibility with the code.

# DEPLOY:

### STEP - 1:
Fork This Repo(Recommanded) or Fork [MLTB](https://github.com/anasty17/mirror-leech-telegram-bot) with all branches or use his public template.

### STEP - 2: (ONLY FOR THOSE WHO FORKED MLTB)
FOR THE PEOPLE WHO FORKED MLTB: 
Go to 'heroku' branch in your forked repo and add these lines in requirements.txt. (MUST else might face errors):
```
aiohttp
asgiref
six
gc-python-utils
cloudscraper
```
ADD below line in `Dockerfile` of heroku branch:
```
RUN apt-get update && apt-get install -y ffmpeg
```
![EXAMPLE](https://telegra.ph/file/0864bc748803c7f14fb3d.png)

### STEP - 3:
Create config.env file using this template. [config_sample.env](https://raw.githubusercontent.com/majnurangeela/mirror-hunter-upstream/tempuse/config_sample.env).

Don't touch `UPSTREAM_REPO` & `UPSTREAM_BRANCH` env vars else all these features won't be there !
Don't Use `ACCOUNTS_ZIP_URL` & `TOKEN_PICKLE_URL` (Broken). Upload accounts folder & token.pickle files in heroku branch

### STEP - 4:
Fill All Action Secrets.

- `HEROKU_API`: Get it from your heroku account.
- `HEROKU_APP_NAME`: Set unique appname.
- `HEROKU_EMAIL`: Heroku Email ID
- `CONFIG_FILE_URL`: Optional ENV.. You can upload config.env on gist or in heroku branch

### STEP - 5:
RUN workflow with heroku branch from GitHub Action section !

## IMPORTANT ! :

For the simplification I've made some terms..

- `UNIFIED` = AppDrive, DriveApp, GDFlix, DriveBit, DriveLinks, DriveSharer, DriveAce, DrivePro Sharer Links
- `UNIFIED_EMAIL`: USE SAME GMAIL ACCOUNT IN ABOVE MENTIONED SHARERS
- `UNIFIED_PASS` : USE SAME PASSWORD IN ABOVE MENTIONED SHARERS

- `HUBDRIVE_CRYPT`: IT WILL BE USED TO BYPASS HUBDRIVE LINKS ONLY.
- `KATDRIVE_CRYPT`: IT WILL BE USED TO BYPASS KATDRIVE, KOLOP, DRIVEHUB LINKS.
- `DRIVEFIRE_CRYPT`: IT WILL BE USED TO BYPASS DRIVEFIRE & DRIVEBUZZ LINKS.

- `XSRF_TOKEN` & `laravel_session`: BOTH COOKIES WILL BE USED TO BYPASS SHARER.PW LINKS.

## CREDITS:
- [Maverick](https://github.com/majnurangeela) for integration and compatibility fixes
- [Anasty17](https://github.com/anasty17/mirror-leech-telegram-bot) for his MLTB & Heroku Bypass !
- [xcscxr](https://github.com/xcscxr) for his wonderful google drive link scrapers !
- [arata74](https://github.com/arata74) or [ANIME-REPUBLIC](https://github.com/ANIME-REPUBLIC) For Base Repo
