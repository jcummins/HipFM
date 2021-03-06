HipFM
=====

Post "now playing" track from last.fm to HipChat room.


## Command line usage

node server.js [last.fm API Key] [last.fm User] [HipChat Key] [HipChat Room] [HipChat Name]

```shell
node server.js THISISMYLASTFMAPIKEY blueflagmusic HIPCHATKEY "My Room" "HipFM"
```

## Config file (hipfm.json) usage

```shell
node server.json -f
```

** Example **

```json
{
    "hipchat": {
        "key": "11111111111111111111111111111111",
        "room": "Music"
    },
    "lastfm": {
        "users": [
            {
                "displayName": "User1Music",
                "username": "lastfm_username1",
                "key": ""
            },
            {
                "displayName": "User2Music",
                "username": "lastfm_user2",
                "key": "11111111111111111111111111111111"
            }
        ]
    }
}
```


* **last.fm API Key**: Get one here [Last.fm Web Services](http://www.last.fm/api/account/create)
* **last.fm User**: The user's playlist you want to follow (eg. [blueflagmusic](http://ws.audioscrobbler.com/1.0/user/blueflagmusic/recenttracks.rss))
* **HipChat Key**: Either an Admin or Notification key. Get one here [https://hipchat.com/admin/api](https://hipchat.com/admin/api)
* **HipChat Room**: The room you want to post to. Must be created in HipChat first.
* **HipChat Name**: _(Optional)_ Name to display in HipChat (usually where the username goes).