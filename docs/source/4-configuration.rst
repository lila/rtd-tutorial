
=============
Configuration
=============

The following environment variables will need to be defined:

GOOGLE_CLOUD_PROJECT
    this points to the GCP project where the application will be deployed

FITBIT_OAUTH_REDIRECT_URL
    this will be the internet accessible location of this app.

FITBIT_OAUTH_CLIENT_SECRET
    provided by Fitbit at http://dev.fitbit.com/ when registering the app

FITBIT_OAUTH_CLIENT_ID
    provided by Fitbit at http://dev.fitbit.com/ when registering the app

GOOGLE_APPLICATION_CREDENTIALS
    json file that holds the service account details for accessing GCP services




Deploying for development
=========================

The above environement variables can be added to `.env`::

    GOOGLE_APPLICATION_CREDENTIALS="<path to json file>"
    GOOGLE_CLOUD_PROJECT = '<your gcp project id>'
    FITBIT_OAUTH_CLIENT_ID = '<your clientid>'
    FITBIT_OAUTH_CLIENT_SECRET = '<your client secret>'
    FITBIT_OAUTH_REDIRECT_URL = 'https://your.domain.com/token'

.. warning:: make sure you don't check this file into the version control system.
