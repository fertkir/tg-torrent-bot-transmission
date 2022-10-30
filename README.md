Ansible Role: tg_torrent_bot_transmission
=========

Integrates [Telegram Torrent Bot](https://www.npmjs.com/package/tg-torrent-bot) with [Transmission bittorrent client](https://transmissionbt.com/).

Thus, you'll be able to search for torrents and download them to your server using Telegram on your cell phone.

Requirements
------------

Any pre-requisites that may not be covered by Ansible itself or the role should be mentioned here. For instance, if the role uses the EC2 module, it may be a good idea to mention in this section that the boto package is required.

Role Variables
--------------

A description of the settable variables for this role should go here, including any variables that are in defaults/main.yml, vars/main.yml, and any variables that can/should be set via parameters to the role. Any variables that are read from other roles and/or the global scope (ie. hostvars, group vars, etc.) should be mentioned here as well.

Dependencies
------------

A list of other roles hosted on Galaxy should go here, plus any details in regards to parameters that may need to be set for other roles, or variables that are used from other roles.

Example Playbook
----------------

Fill in your telegram bot token (get it from [@BotFather](https://t.me/BotFather) telegram bot) and credentials for rutracker.org.

```yaml
- hosts: all
  roles:
    - role: fertkir.tg_torrent_bot_transmission
      vars:
        tg_torrent_bot:
          telegram_token: <your_telegram_token_here>
          rutracker:
            username: <rutracker_username>
            password: <rutracker_password>
```

## License

This project is licensed under GNU General Public License v3.0. See [LICENSE](/LICENSE) for more details.
