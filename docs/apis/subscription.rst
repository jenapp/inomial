============
subscription
============
The subscription REST API posts a structured JSON document to update a subscription.

URL
===

``https://smile.example.com/stage/api/subscription/{id}/update``

Method
======
POST

URL Params
==========
**Required:**

id=[string]

id can be UUID or USN of subscription.

Document Format
===============
**Example:** ::

    {
      "releaseDelay" : 0,
      "timezone" : "Australia/Victoria",
      "username" : "john.adsl@example.com",
      "description" : "The A2 Start D Plan",
      "custom" : {
         "newsletter_subscribe" : true,
         "productDescription" : "3G Wireless Modem"
      }
    }

Subscription attributes
-----------------------

================== =========== ==================================================================================================================================== ==================================
Field name         Data type   Description                                                                                                                          Required?
================== =========== ==================================================================================================================================== ==================================
username           String
description        String
releaseDelay       Number      Default is inherited from account
timezone           String      Full time zone name. 
                               
                               For example: Australia/Adelaide. 
custom             Json object Data is in code/value pairs. Value can be an object or array.
                               
                               For example:
                               {"test_text":"value","is_bool":true,"test_date": “2018-12-08”,”test_number":123.45, “note”: [“Important note1”, “Important note2”]}
                               
                               **Note**: Date must be in yyyy-MM-dd format. 
                               If there is no matching custom field from provided code in Smile, a new one will be created.
================== =========== ==================================================================================================================================== ==================================

Success Response
================
This request returns a subscription ID updated and status

Example:
--------

**Code:** 200 (OK)

**Content:** ::

    { 
       "subscriptionId":"e5f946bb-6b31-4bbd-ae6c-247c54a57b4b",
       "status":"UPDATED"
    }

Error Response
==============

Example:
--------

**Code:** 500 (Internal Server Error)

**Description:** Returned if something fails during an update. You can find more details from the server’s log.

**Content:** ::

    {
       "subscriptionId":"e5f946bb-6b31-4bbd-ae6c-247c54a57b4b",
       "status":"INTERNAL_ERROR"
    }
    
Example:
--------
**Code:** 200

* ``NOT_SUBSCRIPTION``
* ``SUBSCRIPTION_MISSING``
* ``TIMEZONE_NOT_FOUND``
* ``DUPLICATE_USERNAME``

**Content:** ::

    {
       "subscriptionId":"e5f946bb-6b31-4bbd-ae6c-247c54a57b4b",
       "status":"ERROR",
       "errors":[
          "NOT_SUBSCRIPTION",
          "TIMEZONE_NOT_FOUND"
       ]
    }

Sample Call
===========
::

   POST /api/subscription HTTP/1.1
   URL: https://smile.example.com/test/api/subscription/e5f946bb-6b31-4bbd-ae6c-247c54a57b4b/update
   Content-Type:application/json
   Accept:application/json

   {
      "releaseDelay" : 0,
      "timezone" : "Australia/Victoria",
      "username" : "john.adsl@example.com",
      "description" : "The A2 Start D Plan",
      "custom" : {
         "newsletter_subscribe" : true,
         "productDescription" : "3G Wireless Modem"
      }
   }
