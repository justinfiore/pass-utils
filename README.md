# pass-utils
utilities for working with [pass](https://www.passwordstore.org) and multi-field password storage

With the Unix `pass` password manager you can store arbitrary text including multiple lines.

This project makes it easy to store [YAML](http://www.yaml.org/start.html) formatted text in your passwords and then extract certain fields.

The assumptions of this project are that you will store multi-field passwords in `pass` using YAML as the format.

You can do this by running `pass edit <passName>` then putting any YAML content in there.

e.g., one possible format could be:

If this is in your password named: `google`
```yaml
url: https://www.google.com
username: foo
password: bar
```

You could then use:

**Show the username**
```
pass-show -n google -f username
```

**Show the password**
```
pass-show -n google -f password
```

**Show the url**
```
pass-show -n google -f url
```

**Show the whole password file contents**
```
pass-show -n google
```

## Installation

1) Clone this repo
2) Add the `bin` subdirectory to your `PATH`
3) Install the [prerequisites](#prerequisites)

## Prerequisites

1) Download `jq` and add it to your `PATH`
  - https://stedolan.github.io/jq/download/

2) Install `yq` and make sure it is on your `PATH`
  - https://github.com/kislyuk/yq#installation (This requires `python`)




