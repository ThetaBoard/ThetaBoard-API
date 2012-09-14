ThetaBoard-API
==============

Help shape the ThetaBoard API.

Authentication
==============

If you're making a private integration with ThetaBoard for your own purposes, you can use HTTP Basic authentication. This is secure since all requests in the new Basecamp use SSL.

If you're making a public integration with ThetaBoard, you must use OAuth 2. This allows users to authorize your application to use Basecamp on their behalf without having to copy/paste API tokens or touch sensitive login info.

Read the authentication guide to get started.

Making a Request
================

All URLs start with https://api.thetaboard.com/[YOUR-ACCOUNT-ID]/v1/. SSL only. The path is prefixed with the account id and the API version. If we change the API in backward-incompatible ways, we'll bump the version marker and maintain stable support for the old URLs.

To make a request for all the projects on your account, you'd append the projects index path to the base url to form something like https://api.thetaboard.com/[YOUR-ACCOUNT-ID]/v1/boards.json. In curl, that looks like:

`curl -u user:pass -H 'User-Agent: MyApp (yourname@example.com)' https://api.thetaboard.com/123456789/v1/boards.json`

To create something, it's the same deal except you also have to include the Content-Type header and the JSON data:

    curl -u username:password \
      -H 'Content-Type: application/json' \
      -H 'User-Agent: MyApp (yourname@example.com)' \
      -d '{ "name": "My new ThetaBoard!" }' \
      https://api.thetaboard.com/123456789/v1/boards.json`
      
API Endpoints
=============
https://api.thetaboard.com/123456789/v1/users
https://api.thetaboard.com/123456789/v1/boards
https://api.thetaboard.com/123456789/v1/boards/1
https://api.thetaboard.com/123456789/v1/boards/1/columns
https://api.thetaboard.com/123456789/v1/boards/1/labels
https://api.thetaboard.com/123456789/v1/boards/1/users
https://api.thetaboard.com/123456789/v1/boards/1/cards
https://api.thetaboard.com/123456789/v1/boards/1/cards/1
https://api.thetaboard.com/123456789/v1/boards/1/cards/1/checklists
https://api.thetaboard.com/123456789/v1/boards/1/cards/1/checklists/1
https://api.thetaboard.com/123456789/v1/boards/1/cards/1/checklists/1/items
https://api.thetaboard.com/123456789/v1/boards/1/cards/1/checklists/1/items/1
https://api.thetaboard.com/123456789/v1/boards/1/cards/1/comments
https://api.thetaboard.com/123456789/v1/boards/1/cards/1/comments/1
https://api.thetaboard.com/123456789/v1/boards/1/cards/1/uploads
https://api.thetaboard.com/123456789/v1/boards/1/cards/1/uploads/1
https://api.thetaboard.com/123456789/v1/boards/1/cards/1/users
https://api.thetaboard.com/123456789/v1/boards/1/cards/1/users/1