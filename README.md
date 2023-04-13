# InstaHaxx


This program will brute force any Instagram account.

### Support

It

## Requirements

- Python v3.9 or higher
- working proxy list

### Install (Manual Way)

```
pip install pipenv

pipenv --python 3.9

pipenv install
```

## Help (-h/h flag output)

```
usage: main.py [-h] [-u USERNAME] [-p PASSLIST] [-px PROXYLIST] [--prune PRUNE] [--stats] [-nc] [-m MODE]

optional arguments:
  -h, --help            show this help message and exit
  -u USERNAME, --username USERNAME
                        email or username
  -p PASSLIST, --passlist PASSLIST
                        password list
  -px PROXYLIST, --proxylist PROXYLIST
                        proxy list
  --prune PRUNE         prune the database
  --stats               get statistics of the proxies
  -nc, --no-color       disable colors
  -m MODE, --mode MODE  modes: 0 => 32 bots; 1 => 16 bots; 2 => 8 bots; 3 => 4 bots
```

## Proxies

The system needs a list of proxies to work. Once uploaded, proxies are saved into a database

### Upload

Upload a list of proxies into the program. The proxy file must have a format of `ip:port`

`proxies_list.txt`

To upload a list of proxies a similar syntax must be followed.

```
3.238.111.248:80
206.189.59.192:8118
165.22.81.30:34100
176.248.120.70:3128
191.242.178.209:3128
180.92.194.235:80
```

```
python main.py -px <path to proxy list>
```

### Stats

This gives an insight into the health of the proxies in the database.

```
python instagram.py --stats
```

### Prune

This allows the able to get rid of proxies with a score below a given score.<br/>
It is recommended that you run the `--stats` and prune the database of proxies<br/>
who have a proxy score below `Q1`.

```
python instagram.py --prune 0.05
```

Pruning is not a requirement because the the system will automatically learn which proxies perform poorly and stop using them.

### Usage

```
python instagram.py -u <username> -p <passlist>
```

> Made with ?? by AKPR