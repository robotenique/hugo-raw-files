# Personal Website - Hugo

This is a repo for the raw files of my personal website [robotenique.github.io](https://robotenique.github.io), built using:

- [Hugo](https://gohugo.io)  framework - version `0.68.3`
- [Hyde-hyde](https://github.com/htr3n/hyde-hyde) theme

## Installation


This repo actually contains the main website code + two git submodules. To correctly develop the website you need to have all submodules in place.

1. Clone this repo
2. You need to also update the submodules. For this, run:

```sh
$ git submodule update --init
```

Make sure that there are files inside the folder `theme/hyde-hyde`. This folder points out to this repo: [https://github.com/robotenique/hugo-theme](https://github.com/robotenique/hugo-theme) that I had to create based on the official hyde-hyde repo because I wanted to change some stuff there. (So if this doesn't work, you can always manually clone it).

The `public` folder might not be crated right now. This is ok, we'll create it later.

3. Install Hugo version `0.68.3`: [https://github.com/gohugoio/hugo/releases/tag/v0.68.3](https://github.com/gohugoio/hugo/releases/tag/v0.68.3)

Check the version with
```sh
$ hugo version
```

4. Try to build the website and run a server with:

```sh
$ hugo server --watch
```

and opening it in a browser. Everything here should be ok as equal as the live website.

5. Manually clone the live website repo:

You need to clone from here: [https://github.com/robotenique/robotenique.github.io](https://github.com/robotenique/robotenique.github.io), but **rename the folder to `public`**. This will be where we'll put the built website and commit live.


Done!

## Usage

That's it! Now, to build a new website version, modify the pages, add new stuff, etc. Then once you want to deploy just run:

```sh
$ ./deploy.sh <commit message>
```

This will build the website into the `public` folder and commit it to its respective repo.

Finally, you also have to commit the changes you did to this repo, where the raw hugo files are kept. Just manually run a git commit and git push.
