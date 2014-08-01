# Dotfiles Sync

This is a very simple script to keep my dotfiles always in sync.

### How to install

1. Clone the project into your home folder
2. Remove the ".example" from "config/dotfiles.example" and add your own dotfiles to monitor
3. Add this line to your ".bash_profile"

```bash
sh ~/.dotfiles_sync/check
```

You probably want to add the check **before** you actually load your dotfiles so, when you initialise them, they will be already updated.

### How it works

The check will happen once a day and will perform the following actions:

1. Check if the dotfiles are present
2. Check if you have changes uncommitted
3. Check if you have commits not pushed to master
4. Check if you have changes on master that needs to be pulled. If yes, it'll ask you if you want to pull them right away.

### Motivation

I usually like to keep my bash files separated from my vim files, even though they are both committed to Github. I also have more than one machine and I found really difficult to keep them all in sync.

I know that there are other similar projects out there but, this project was also an excuse to build my own bash functions that can be composed by bash piping and have some fun.

Feedbacks are welcome. =)
