# Calvin's Documentation

This is my personal documentation written in Sphinx!

It is hosted on Read the Docs at [http://calvin.rtfd.io](http://calvin.rtfd.io).

Read the Docs has a webhook which should build the documentation after a push to GitHub.

## Install Sphinx

Assuming you have Python already, install Sphinx:

`$ pip install sphinx sphinx-autobuild sphinx_rtd_theme`

## Running

With everything installed, click on serve.bat for an auto-builder.

After it's built, go to [http://localhost:8000](http://localhost:8000).

## Decrypt and Encrypt using OpenSSL

I have encrypted secrets using OpenSSL.

To decrypt them:

`cat secret.txt | openssl enc -d -aes-256-cbc -a -salt`
`echo secret | openssl enc -d -aes-256-cbc -a -salt`

To encrypt secrets:

`cat secret.txt | openssl enc -e -aes-256-cbc -a -salt`
`echo secret | openssl enc -e -aes-256-cbc -a -salt`
