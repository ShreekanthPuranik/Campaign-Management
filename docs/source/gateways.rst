
.. _gateways
Gateways
============

**Get All Gateways From All clusters**

   **Request**

   .. list-table:: 

     * - **Method**
       - **URL**
     * - GET
       - /api/gateways


   **Response**

   .. raw:: html

      <small style="font-size: 14px;"><strong>200</strong></small>

   .. code-block:: python

       {
            "status_code": int,
            "data": [
               {
                     "cluster_name": string,
                     "gateways": [
                        {
                           "name": string,
                           "did_range": string
                        }
                     ]
               }
            ]
       }

