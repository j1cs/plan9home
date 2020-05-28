# Plan9 user home files
Here are my custom configuration for my plan9 box!
The devices I'm using is an Samsung ATIV Smart PC Pro XE700T1C and laptop PC!

To clone into your plna9front box you need to have installed https://github.com/oridb/git9 a git implementation of git for plan9. 

configure your ssh key:

auth/rsagen -t 'service=ssh role=client' >githubkey
auth/rsa2ssh githubkey # put this into github management keys
cat githubkey >/mnt/factotum/ctl

Then run
 git/clone ssh://git@github.com/glats/plan9home

You are done!

