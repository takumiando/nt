# nt

```nt``` is a simple note script in POSIX shell.

## Usage

### Init

Set your git repository to sync your notes.

```
$ nt
Initialized empty Git repository in /home/takumi/.nt/.git/
Switched to a new branch 'main'
Git repository URL: git@github.com:takumiando/notes.git
remote: Enumerating objects: 15, done.
remote: Counting objects: 100% (15/15), done.
remote: Compressing objects: 100% (10/10), done.
remote: Total 15 (delta 3), reused 15 (delta 3), pack-reused 0
Unpacking objects: 100% (15/15), 2.12 KiB | 543.00 KiB/s, done.
From github.com:takumiando/notes
 * branch            main       -> FETCH_HEAD
 * [new branch]      main       -> origin/main
```

### Write

You can write from args and stdin.

```
$ nt hogehoge fugafuga
```

```
$ ls | nt
```

### Read

```
$ nt
2021/12/02 17:10:16 hogehoge fugafuga
```

### Delete

Not implemented yet.

### Sync

```
$ nt -s
From github.com:takumiando/notes
 * branch            main       -> FETCH_HEAD
 Already up to date.
 [main b5cf9b5] Update bonanza
  1 file changed, 25 insertions(+)
 Enumerating objects: 5, done.
 Counting objects: 100% (5/5), done.
 Delta compression using up to 8 threads
 Compressing objects: 100% (3/3), done.
 Writing objects: 100% (3/3), 571 bytes | 571.00 KiB/s, done.
 Total 3 (delta 0), reused 0 (delta 0), pack-reused 0
 To github.com:takumiando/notes.git
    7951dad..b5cf9b5  main -> main
```
