## What is that?

System locale: specifies the language of system services and graphical interfaces
Keyboard layout: specifies the layout used in text console and graphical interfaces
<br>

## How to change the system locale

### Editing /etc/locale.conf

You can edit /etc/locale.conf file. This file is read at boot by systemd daemon.
All services and users inherit this configuration and some users or services can override them.
You can see some configuration options in the table below

| OPTION | Description |
|---|---|
| `LANG` | System locale default value |
| `LC_COLLATE` | Change how functions compare strings |
| `LC_NUMERIC` | Change how numbers are print |
| `LC_TIME` | Change the display of current time |
| `LC_MESSAGES` | Change the language of system error output mensages |

And, below you can see a sample

```
LANG=pt_BR.UTF-8
LC_MESSAGES=C
```

In this sample system language is defined as Portuguese (Brasil) and system messages in English.

### Using localectl command

You can use the localectl command to get and set system locale and keyboard layout. 
A list of commands is show below:

|localectl commands|

| COMMAND | Description |
|---|---|
| `localectl status` | List current settings |
| `localectl set-locale [localectl option]=[value]` | Change a localectl.conf variable value. You can use this to configure all options avaliable in locale.conf file

Here a sample to set locale configuration

```
localectl set-locale LANG=en_AU
```

### Changing keymap


