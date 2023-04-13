# InstaHaxx


this software will brute force any Instagram account.


## Tutorial

### Requirements

- python v3.9 or higher
- working proxy list

### Install (Manual Way)

```
pip install pipenv

pipenv --python 3.9

pipenv install
```

### Usage

```
python instahaxx.py -u <username> -p <passlist>
```

## Help (-h/h flag output)

```
usage: instahaxx.py [-h] [-u USERNAME] [-p PASSLIST] [-px PROXYLIST] [--prune PRUNE] [--stats] [-nc] [-m MODE]

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

the system needs a list of proxies to work. proxies are saved into a database by uploading

### Upload

Upload a list of proxies into the program. the proxy file must have a format of `ip:port`

```
python main.py -px <path to proxy list>
```

#### Example

```
3.238.111.248:80
206.189.59.192:8118
165.22.81.30:34100
176.248.120.70:3128
191.242.178.209:3128
180.92.194.235:80
```

### Stats

this gives an insight into the health of the proxies in the database.

```
python instahaxx.py --stats
```

### Prune

this allows the ability to get rid of proxies with a score below a given score. it is recommended that you run the `--stats` and prune the database of proxies. who have a proxy score below `Q1`.
pruning is not a requirement because the the system will automatically learn which proxies perform poorly and stop using them.
```
python instahaxx.py --prune <score in integer value>
```
