# Plan9 user home files
Here are my custom configuration for my plan9 box! (aka dotfiles)

## Using git9 

git9 is a command for use repos from any git server in your plan9front machine. Was wrie from scracth (no a port!).  
more info: https://github.com/oridb/git9  
To install it you can do this:
```
% cd /sys/
% hg clone https://code.9front.org/hg/ports/
% cd ports/dev-vcs/git9/
% mk install
```
## Configure ssh key
```
% auth/rsagen -t 'service=ssh role=client' >githubkey
% auth/rsa2ssh githubkey # the result put it in your git server (i.e github gpg and sshk key manager)
% cat githubkey >/mnt/factotum/ctl
```
Then run  
```% git/clone ssh://git@github.com/glats/plan9home```

You are done!

