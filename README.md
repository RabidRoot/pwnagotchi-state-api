# pwnagotchi State Api

Throw it into the plugins directory. 

## Configuration

```
    state-api:
      enabled: true
      theme: minimal # optional - can be minimal or darkmode. Is state.html if left out.
```

It takes information from the display state, as well as the `/api/v1/mesh/data` and `/api/v1/mesh/peers` providers. 

Call `/plugins/state-api/display` to retrieve the default page

Call `/plugins/state-api/` to retrieve the state JSON

### Sample response:
```
{
    "aps":"1 (29)",
    "channel":"*",
    "cpu":0.24692407498545926,
    "epoch":2,
    "face":"(\u2609_\u2609 )",
    "friend_face_text":"(\u2609_\u2609 )",
    "friend_name_text":"\u258c\u258c\u258c\u258c bunny 17 (52)",
    "identity":"dc8fae09de6333330de1da2077f7133e5ed66bff3ee72ad499eb911a84be3ce1",
    "memory":0.8,
    "mode":"  AI",
    "name":"chiba",
    "num_peers":1,
    "peers":
        [{
        "face":"( \u2686_\u2686)",
        "identity":"5a333337551174eb033ee5f2d2e07271c57946cfcf7655dd3019eb3e2ce10",
        "name":"bunny",
        "pwnd_run":17,
        "pwnd_tot":52
        }],
    "pwnd_run":2,
    "pwnd_tot":34,
    "status":"...",
    "temperature":43,
    "uptime":"01:55:16",
    "version":"1.2.1"
}
```

## I Want to make my own theme!

state.html is a good start. Name your file `state-{name_of_theme}.html`

For example, I renamed state.html to state-darkmode.html and set the background and color CSS. Have fun!

## TODO
`GET /api/v1/inbox https://pwnagotchi.ai/api/local/#get-api-v1-inbox` - get any unread messages and/or total messages

## Default page based on JSON being returned

![alt text](https://github.com/dipsylala/pwnagotchi-state-api/blob/master/images/screen.gif "Animated Pwnagotchi HTML page")

## Example minimal version

![alt text](https://github.com/dipsylala/pwnagotchi-state-api/blob/master/images/minimal.gif "Minimal themed Pwnagotchi HTML page")

