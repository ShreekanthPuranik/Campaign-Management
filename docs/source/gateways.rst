
.. _gateways
Gateways
============

1. Get All Gateways From All clusters
-----------------------------------------


   **Request**

   .. list-table:: 

     * - **Method**
       - **URL**
     * - GET
       - /api/gateways


   **Response**

   .. list-table:: 

     * - **Status**
       - **Response**
     * - 200
       - ``{
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
         }``

