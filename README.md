ThetaBoard-API
==============

Help shape the ThetaBoard API.

Making a Request
================

All URLs start with https://api.thetaboard.com/[YOUR-ACCOUNT-ID]/v1/. SSL only. The path is prefixed with the account id and the API version. If we change the API in backward-incompatible ways, we'll bump the version marker and maintain stable support for the old URLs.

To make a request for all the projects on your account, you'd append the projects index path to the base url to form something like https://api.thetaboard.com/[YOUR-ACCOUNT-ID]/v1/boards.json. In curl, that looks like:

`curl -u user:pass -H 'User-Agent: MyApp (yourname@example.com)' https://api.thetaboard.com/123456789/v1/boards.json`

To create something, it's the same deal except you also have to include the Content-Type header and the JSON data:

`curl -u username:password \
  -H 'Content-Type: application/json' \
  -H 'User-Agent: MyApp (yourname@example.com)' \
  -d '{ "name": "My new ThetaBoard!" }' \
  https://api.thetaboard.com/123456789/v1/boards.json`

Authentication
==============

If you're making a private integration with ThetaBoard for your own purposes, you can use HTTP Basic authentication. This is secure since all requests in the new Basecamp use SSL.

If you're making a public integration with ThetaBoard, you must use OAuth 2. This allows users to authorize your application to use Basecamp on their behalf without having to copy/paste API tokens or touch sensitive login info.

Read the authentication guide to get started.

Table of Contents
=================