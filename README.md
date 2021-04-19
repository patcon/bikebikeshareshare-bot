# bike bike share share bot

A bot for watching a Signal messenger group, and sharing bikeshare pin codes for those who ask.

Currently it is preparing to detect shared location pins with variants of ":bike::pray:" in the description.

## To Do

- [x] get signal-cli working
- [x] detect messages
- [x] extract latitude and longitude
- [ ] talk to bikeshare api with auth token
- [ ] find nearest station
- [ ] get ride code
- [ ] do real user/pass auth with bikeshare api
- [ ] figure out dbus messaging bus

## Usage

```
$ pipenv install
$ cp sample.env .env
$ vim .env
$ pipenv run python check.py --help

Usage: check.py [OPTIONS]

  Check messages in a Signal group for Bikeshare Toronto code requests.

Options:
  -u, --bikeshare-user TEXT       Bikeshare Toronto member account username
                                  (not yet functional)

  -p, --bikeshare-pass TEXT       Bikeshare Toronto member account password
                                  (not yet functional)

  -t, --bikeshare-auth-token TEXT
                                  Bikeshare Toronto member account derived
                                  authorization token  [required]

  -k, --bikeshare-api-key TEXT    Bikeshare Toronto application API key
                                  [required]

  -g, --signal-group TEXT         Signal messengers group ID  [required]
  --noop                          Fake contact to Bikeshare servers
  -d, --debug                     Show debug output
  -h, --help                      Show this message and exit.
```
