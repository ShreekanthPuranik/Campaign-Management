
.. _authentication

Authentication
-----------------

Each request to the API must have a cookie specified below.

   **cookies**

   .. list-table:: 

     * - **Name**
       - **Values**
     * - Botstream_monitor
       - <token>

   **Example**

   The token can be requested from IraAuth and is described in the example below.

   .. code-block:: 

      curl -X POST https://auth.epicode.in/hydra/oauth2/token \
      -d client_id=<client_id> \
      -d client_secret=<client_secret> \
      -d grant_type=client_credentials \
      -d scope=api

   Making a request to the above endpoint by providing the client ID and secret will return you the token and this token can be used for a limited period of time.
   Upon expiry, you will need to renew the token by calling this endpoint again.

   Once you obtain the token, you can make the request as given below.

   .. code-block:: 

      curl https://analytics.epicode.in/botstream_monitor/api/campaign-list \
      -b botstream_monitor=<token>

   It is recommended to use the OAuth2 client libraries rather than dealing with it on your own. If you are using python, use the IraAuthM2M library **(https://pypi.org/project/ira-auth-m2m-client/0.1.0/)**
   which handles authentication and token renewal.

.. autosummary::
   :toctree: generated

   lumache
