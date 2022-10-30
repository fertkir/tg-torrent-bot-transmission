Ansible Role: tg_torrent_bot_transmission
=========

Integrates [Telegram Torrent Bot](https://www.npmjs.com/package/tg-torrent-bot) with [Transmission bittorrent client](https://transmissionbt.com/).

Thus, you'll be able to search for torrents and download them to your server using Telegram on your cell phone.

Requirements
------------

* systemd

Role Variables
--------------

All variables which can be overridden are stored in [defaults/main.yml](defaults/main.yml) file as well as in table below.

| Name           | Default Value | Description                        |
| -------------- | ------------- | -----------------------------------|
| `telegram_token` | | Telegram bot token, get it from [@BotFather](https://t.me/BotFather) |
| `rutracker_host` | https://rutracker.org | You can set your own rutracker mirror here. |
| `rutracker_username` | | Username for access to rutracker.org |
| `rutracker_password` | | Password for access to rutracker.org |
| `allowed_users` | "" | Comma-separated list of users, with whom the bot will work. If empty, the bot will respond to any user. |
| `proxy_telegram` | false | Should the bot use proxy to access Telegram servers |
| `proxy_rutracker` | false | Should the bot use proxy to access rutracker.org |
| `proxy_host` | 127.0.0.1 | Proxy host |
| `proxy_port` | 8080 | Proxy port |
| `proxy_username` | "" | Proxy username |
| `proxy_password` | "" | Proxy password |

Example Playbook
----------------

Fill in your telegram bot token (get it from [@BotFather](https://t.me/BotFather) telegram bot) and credentials for rutracker.org.

```yaml
- hosts: all
  roles:
    - role: fertkir.tg_torrent_bot_transmission
      vars:
        telegram_token: <your_telegram_token_here>
        rutracker_username: <rutracker_username>
        rutracker_password: <rutracker_password>
```

## License

This project is licensed under GNU General Public License v3.0. See [LICENSE](/LICENSE) for more details.
