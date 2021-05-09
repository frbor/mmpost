# mmpost

Post message to mattermost from command line.

# Installation

```bash
sudo pip3 install mmpost
```

# Configuration

`mmpost` can be configured using both command line arguments and a configuration file, or a combination of both.

This configuration file can be put in $XDG_CONFIG_HOME/mmpost/config (normally ~/.config/mmpost/config):

```
[DEFAULT]

# Mattermost server
server = <SERVER>

# Mattermost server
port = 443

# Mattermost token
token = <TOKEN>

# Mattermost team name
team = <TEAM>

# Mattermost channel
channel = <MATTERMOST CHANNEL>

# Mattermost message
message = <MESSAGE TO POST>

# Skip SSL-verify (set to True to skip SSL verification)
no-verify=

```

Normally you would configure server, token, team (and channel) and only specify --message on command line.

If `message` is not configured, it will read from stdin. If empty value is passed to stdin, nothing will be posted.
