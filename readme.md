# Switchboard's Email Design Workflow

Forked from Lee Munroe's [dopesauce workflow](https://github.com/leemunroe/grunt-email-design).

## What's it do?

This grunt task helps simplify things at the design stage.

1. Compiles your SCSS to CSS

2. Builds your HTML and TXT email templates from handlebars.

3. Inlines your CSS

4. Sends a test email (optional - needs config)

## Changes from the original.

The [original README](https://github.com/leemunroe/grunt-email-design) is much more informative. You should read it.

However, I did make a few changes.

* All depedencies that are prefixed with `grunt-` are automatically loaded into Grunt using [matchdep](https://www.npmjs.com/package/matchdep).

* We are using [Ink by Zurb](https://github.com/zurb/ink). (Hence, I removed Lee's original `SASS` and layout.)


## TODO

Build a step to upload media to an s3bucket. Lee's original implementation used rackspace.

## Requirements

* Node.js - [Install Node.js](https://github.com/joyent/node/wiki/Installing-Node.js-via-package-manager)
* Grunt-cli and Grunt (`npm install grunt-cli -g`)
* Ruby - [Install ruby with RVM](https://rvm.io/rvm/install)
* Premailer (`gem install premailer hpricot nokogiri`) - Inlines the CSS
* [Mailgun](http://www.mailgun.com) (optional) - Sends the email
* [Litmus](https://litmus.com) (optional) - Tests the email across all clients/browsers/devices
