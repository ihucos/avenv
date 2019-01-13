# avenv
A more isolated virtualenv

## Install / Update
```
curl --fail --location https://github.com/ihucos/avenv/raw/master/avenv-dist.tar | tar -xf - -C /usr/local/bin/
```

### How to use
Just exactly like virtualenv (but it's called `avenv`)

### What is this ?
It's basically a lightweight replacement for containers in the interface of `virtualenv`, so you don't need to learn new stuff.

### Why should I use it?
More isolation. You don't even need to have python installed.

### Linux only support
Tell your employer to stop using Macintosh

### No Python 2 support
Life is no Ponyhof. It's over, no Python 2 support.

### I can't setuid/setgid inside my container
Ensure you have newuidmap/newgidmap installed and that our user have some
uids/gids in /etc/subuid and/or /set/subgid. Apt for example needs this.

### Does it run LibreOffice?
Of course
```
$ avenv venv # initialize the virtualenv
...
$ venv/bin/apt-get update # you can imagine that as kind of like a chrooted ubuntu linux
...
$ venv/bin/avenv-update # remap all executables in a PATH to venv/bin so you can call them comfortably
$ venv/bin/libreoffice # run libreoffice
```

### Could I use this for other stuff?
Yes, it's kind of based on this: https://github.com/ihucos/bchroot

*cough* *cough* click on my super awesome container engine I want people to use: https://github.com/ihucos/plash *aham*
