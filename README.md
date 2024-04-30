# Overview

`config.yaml` defines bot configuration. You can have your own bot with your own config file, keep the bot code up to date with the [origin][1] and just use your own repo with your own config for the bot.


# Currently available configuration options:

- `ban_add_poll_results`: defines how many people from your chat need to reply to poll in order to add phrase to the list of banned phrases.
    - `no_maximum_count`: integer. If given number of chat members will reply `no`, then phrase won't be banned. For example, if you specify here `2`, and during the poll 2 members of chat will reply 'No', then poll will be stopped and phrase won't be added to the ban list.
    - `yes_minimum_count`: integer. Opposite to `no_maximum_count`. If given number of chat members will reply `Yes`, then poll will be stopped and phrase will be added to the banned list.
- `banned_phrases`: list of strings. If any member of chat (except administrators) will send message with any of these messages, bot will ban this user. List of phrases is maintained by the bot with polls (see `/ban_add` command in the bot's README).
- `footer`: defines a footer for `/help` or `/info` command.
    - `print`: bool. If true, footer will be printed.
    - `text`: html string. Defines what will be printed.



[1]: https://github.com/doatta/simple-tgbot