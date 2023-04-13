# nt

```nt``` is a very simple CLI note in POSIX.

You can store and sync your texts with [GitHub Gist](https://gist.github.com/).

## Requrements

* ```curl```
* ```jq```(reluctantly...)

## Setup

You need to set [Gist ID](https://docs.github.com/en/get-started/writing-on-github/editing-and-sharing-content-with-gists/creating-gists) and [User Token with only gist permission](https://docs.github.com/en/authentication/keeping-your-account-and-data-secure/creating-a-personal-access-token) in ```~/.ntrc```.

```Shell
GIST_ID=YOUR_GIST_ID
USER_TOKEN=YOUR_USER_TOKEN
```

```install``` copies to ```/usr/local/bin``` by default.

```ShellSession
$ sudo ./install
```

But you can install ```nt``` to everywhere that you want.

## Usage

### Write

#### From arguments

```ShellSession
$ nt "I really want to stay at your house"

20230413_141802

    I really want to stay at your house

```

#### From pipe

```ShellSession
$ printf "I really want to stay at your house\n" | nt

20230413_141802

    I really want to stay at your house

```

#### From redirection

```ShellSession
$ nt < lyrics.txt

20230413_141802

    I really want to stay at your house

```

#### From heredoc

```ShellSession
$ nt << EOF
I really want to stay at your house
EOF

20230413_141802

    I really want to stay at your house

```

### Read

```ShellSession
$ nt

20230413_141802

    I really want to stay at your house

20230413_142012

    And I hope this works out

20230413_142020

    But you know how much you broke me apart

20230413_142030

    I'm done with you, I'm ignoring you, I don't wanna know

(END)
```

### Delete

```ShellSession
$ nt -d 20230413_142020

20230413_141802

    I really want to stay at your house

20230413_142012

    And I hope this works out

20230413_142030

    I'm done with you, I'm ignoring you, I don't wanna know

(END)
```

### Save to local

```ShellSession
$ nt > note.txt
```
