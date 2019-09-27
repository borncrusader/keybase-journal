## About
This is a framework for a journal to be used with keybase. The idea is to
maintain journal entries in a git repository under keybase.

## Keybase
[Keybase](https://keybase.io) is a key directory that maps identities of people
across different social media and website to a set of public keys. It also lets
you store a set of public files and of course a set of private files that are
only available to you.

Checkout [Wikipedia](https://en.wikipedia.org/wiki/Keybase) for more details.

## What's Keybase Git
The private files that you can store in keybase can also be versioned as a git
repository. Essentially, keybase adds a git commit hook that would encrypt your
files using the private key on your local machine and send the encrypted blob
to the keybase server. Thus, all your files are end-to-end encrypted and you
can be happy that none of your files in the git repo are readable by external
parties, including keybase.

More on this [here](https://keybase.io/blog/encrypted-git-for-everyone).

## Why store journal entries in Keybase?
I'm not going to explain why journaling is important. :) A great deal has been
said about journaling already. Just know that journaling is a form of
stretching for your brain. It is cathartic and relaxes your brain after a long
hard day's work.

I used to store all my journal entries on Dropbox like many others but over
time I realized that I was adding more and more content that I deemed personal
and I don't want to share that with anyone. Plus, Dropbox started limiting its
free tier to just 3 devices and I realized I wanted an alternative.

Enter keybase! :)

## What's in it?
This journaling system is built around
[mdbook](https://github.com/rust-lang-nursery/mdBook) which is a rust-based
system to write books. This repository is ideally just a wrapper around
`mdbook`, integrating it with keybase.

## How does this work?

    1. Clone the repository
    2. Run `./journal prepare` for the first time
    3. The format for every journal is stored in `src/format/`
    4. Run `./journal today` to create an entry for today. This would
       automatically open an editor for you. The default `EDITOR` is configured
       as [Typora](https://typora.io/) which is a truly remarkable editor. Feel
       free to change this as you please.

## How to export as a book?
TODO

## How do I contribute?
PRs welcome, of course!
