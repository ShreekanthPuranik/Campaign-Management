
.. _index
Campaign
===============

1. Create Campaign
----------------------

   **Request**

   .. list-table:: 

     * - **Method**
       - **URL**
     * - Post   	
       - /api/campaign	


   **Body**

   .. code-block:: json

    {
        "name": "string",
        "clusters": [
            {
                "cluster_name": "string",
                "capacity": "int",
                "weightage": "int",
                "gateways": [
                    {
                        "name": "string",
                        "did_range": "string"
                    }
                ]
            }
        ]
    }

   **Response**

   .. raw:: html

      <small style="font-size: 30px;">200</small>

   .. code-block:: json

    {
             "status_code": int, 
             "status": string
    }


2. Update Campaign
--------------------

   **Request**

   .. list-table:: 

     * - **Method**
       - **URL**
     * - PUT
       - /api/campaign 

   **Body**

   .. code-block:: json

    {
        "name": "string",
        "clusters": [
            {
                "cluster_name": "string",
                "capacity": "int",
                "weightage": "int",
                "gateways": [
                    {
                        "name": "string",
                        "did_range": "string"
                    }
                ]
            }
        ]
    }


   **Response**

   .. list-table:: 

     * - **Status**
       - **Response**
     * - 200
       - {"status_code": int, "status": string}


3. Delete Campaign
------------------------

   **Request**

   .. list-table:: 

     * - **Method**
       - **URL**
     * - DELETE 
       - /api/campaign


   **Body**

   .. code-block:: 

      ""data" : {
            "name" : string
       }

   **Response**

   .. list-table:: 

     * - **Status**
       - **Response**
     * - 200
       - {"status_code": int, "status": string}


4. Get all campaigns
------------------------

   **Request**

   .. list-table:: 

     * - **Method**
       - **URL**
     * - GET 
       - /api/campaign-list

   **Response**

   .. list-table:: 

     * - **Status**
       - **Response**
     * - 200
       - {
                  "status_code": "int",
                  "data": [
                      {
                          "name": "string",
                          "clusters": [
                              {
                                  "cluster_name": "string",
                                  "capacity": "int",
                                  "weightage": "int",
                                  "gateways": [
                                      {
                                          "name": "string",
                                          "did_range": "string"
                                      }
                                  ]
                              }
                          ]
                      }
                  ]
              }

5. Get Campaign
--------------------

   **Request**

   .. list-table:: 

     * - **Method**
       - **URL**
     * - GET
       - /api/campaign/{id}


   **Path Parameters**

   .. list-table:: 

     * - **Params**
       - **Values**
     * - id
       - string


   **Response**
   
   .. list-table:: 

     * - **Status**
       - **Response**
     * - 200
       - {
            "status_code": int,
            "data": {
                "name": "string",
                "clusters": [
                    {
                        "cluster_name": "string",
                        "capacity": "int",
                        "weightage": "int",
                        "gateways": [
                            {
                                "name": "string",
                                "did_range": "string"
                            }
                        ]
                    }
                ]
            }
         }


.. autosummary:: 
.. toctree:: generated
   :numbered:

   index
   gateways
   authentication