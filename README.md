[![PyPI version](https://badge.fury.io/py/dropbox-py3.svg)](http://badge.fury.io/py/dropbox-py3)

A note from the forker
======================

This repo is a fork of the official Python Dropbox SDK created to make it python 3 compatible, and provide the fix to the community. I will only fix the parts that are blocking me on my own project, but feel free to submit pull request if you find other part. If you're from Dropbox, of course, feel free to backport fixes frop this repo to the original dropbox repo.
I'll try to keep the pypi version up to date with the various fixes proposed here, so that we can all simply pip install dropbox-py3 in our own py3 projects :)

Note : for me, the test won't pass as-is, either for py27 or py34. I initially wanted to add a tox.ini to test both versions, but what I really want is for this to work in my project, I don't really have the time to also fix all the tests that did not originally pass. That said, if you do, feel free.

Warning : I am NOT a Dropbox person and I am not affiliated with Dropbox. I don't claim any ownership to this code and all the modification are made according to the MIT license distibuted with the original Dropbox package. I'm not a licensing expert so I don't know the legal status of the modifications themselves in this fork but , as far as I understand, these modification being written under the MIT license let them be used back in the original project or in any other project if need be. Please contact me ( @ewjoachim ) if there's a problem with that, and keep all of that in mind if you add a merge request. Thanks.

Final note : Hey Dropbox, I really like what you do, but I don't get why you released the source of this with an MIT license and didn't do a Github repo as you do with other software you opensource. Thnik about it ...? Have a nice day (and keep being awesome !). And if at some point you can merge this project or add the equivalent features in the original package, We'd all be thankful.

Related stuff :

 - Original : https://pypi.python.org/pypi/dropbox
 - Fork : https://pypi.python.org/pypi/dropbox-py3
 - Originating discussion : https://twitter.com/smarx/status/600082229197479938

Dropbox Core SDK for Python
===========================

A Python library for Dropbox's HTTP-based Core and Datastore APIs.

- https://www.dropbox.com/developers/core/docs
- https://www.dropbox.com/developers/datastore/docs

Setup
-----

You can install this package using ``pip``::

   $ pip install dropbox

Getting a Dropbox API key
-------------------------

You need a Dropbox API key to make API requests.

- Go to https://dropbox.com/developers/apps.
- If you've already registered an app, click on the "Options" link to see the
  app's API key and secret.
- Otherwise, click "Create an app" to register an app. Choose "Dropbox API"
  with datastore and/or file permissions depending on your needs.
  See https://www.dropbox.com/developers/reference#app-permissions.

Using the Dropbox API
---------------------

Full documentation:

- https://www.dropbox.com/developers/core/docs
- https://www.dropbox.com/developers/datastore/docs

Before your app can access a Dropbox user's files, the user must authorize your
application using OAuth 2.  Successfully completing this authorization flow
gives you an "access token" for the user's Dropbox account, which grants you the
ability to make Dropbox API calls to access their files.

- Authorization example for a web app: example/flask_app/
- Authorization example for a command-line tool:
  https://www.dropbox.com/developers/core/start/python

Once you have an access token, create a DropboxClient instance and start making
API calls.

You only need to perform the authorization process once per user.  Once you have
an access token for a user, save it somewhere persistent, like in a database.
The next time that user visits your app, you can skip the authorization process
and go straight to making API calls.

Running the Examples
--------------------

There are example programs in the "example" folder.  Before you can run an
example, you need to edit the ".py" file and put your Dropbox API app key and
secret in the "APP_KEY" and "APP_SECRET" constants.
