# Rising

This is a [TiddlyWiki](https://tiddlywiki.com) template with some useful defaults:

* Comes with some tools for adding light, easy-to-use organization using templates
* Comes with some simple macros (including macros for making and documenting simple macros)
* Looks more like something made by a human being

## Setup

The tricky part with any TiddlyWiki is making it easy to save your changes. I recommend using a
GitHub Pages repo under a separate account from your normal one. It’s simpler to set up than other
methods, and when the setup is done, you can edit and save changes from any device. The separate account is
useful both for secrecy and because any usage creates lots of commits that might feel like noise to
you or your followers.

### Set up the GitHub Pages site

Set up a secret, burner GitHub account. Log into this new account and [create a GitHub Pages
site][1] repo.

Add the `index.html` and `.nojekyll` files from this repo to the one you just made.

Still in your new GitHub account, go to the account settings and click Developer Settings → Personal
access tokens → Fine-grained tokens, and click **Generate new token**.

* Set the token to expire in a year (the max allowed).
* Under *Repository Access* click *Only select repositories* and select your GitHub Pages repo.
* Under *Permissions* you only need to add one: enable “Read and write” for *Contents*. (This will
  automatically add read permissions for “Metadata”.)

Click **Generate token**. Copy/paste the new token into your password manager.

### Plug in credentials so you can save your changes

At this point you can visit the site and even edit it, but your changes will not be saved.

Open your GitHub Pages site in your browser.

Click the gear icon at the top to open the Control Panel, then click the *Saving* tab → *GitHub
Saver* and fill in the fields:

* “Username” should be the username of your burner GitHub account
* “Password, OAUTH token, or personal access token”: paste in the secret token you generated above
* “Target repository” should be your username and repo name in the format `username/repo`.
* “Target branch for saving” is usually `main`.
* “Path to target file” should be just `/` unless you have stored `index.html` in a subfolder of the
  repo.
* “Filename of target file” is `index.html`.
* “Server API URL” should be `https://api.github.com`.

Once this is filled out, close the Control Panel card and try editing something, or creating a new
card. You should see a small “Saved wiki” notification appear momentarily in the top right.

*Et voilà!* You have a personal wiki that is nice to look at and globally accessible for free.

If you want to be able to save changes from another browser or device, you’ll need to open the site
on that device and enter the personal access token in the settings just like you did above (the rest
of the settings.

### Add the site to your iOS home screen

Open the GitHub Pages site in Safari. Tap the Share icon (box with an arrow coming out) and tap
**Add to Home Screen**.

Tap the new home screen icon to open the site as a web app on your phone. Again, remember to add the
personal access token in the settings here so you can save changes from your phone.

[1]: https://docs.github.com/en/pages/getting-started-with-github-pages/creating-a-github-pages-site
