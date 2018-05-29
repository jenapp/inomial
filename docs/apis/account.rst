=======
account
=======
The account REST API posts a structured JSON document to update an account.

URL
===

``https://smile.example.com/stage/api/account/{id}/update``

Method
======
POST

URL Params
==========
**Required:**

id=[string]

id can be UUID or USN of account.

Document Format
===============
**Example:** ::

    {
       "taxable" : true,
       "releaseDelay" : 0,
       "comments" : "Comments",
       "contactTitle" : "MR",
       "givenName" : "Alfred",
       "familyName" : "Sample",
       "abn" : "94 088 172 301",
       "serviceAddress" : {
          "addressDetail" : "Main Building",
          "streetNumber" : "120",
          "streetType" : "Road",
          "streetName" : "Main",
          "suburb" : "Melbourne",
          "country" : "Australia",
          "postcode" : "3000"
       },
       "companyName" : "Example Telecom",
       "tradingName" : "Example Telco",
       "billAddress" : {
          "streetNumber" : "620",
          "streetType" : "Street",
          "streetName" : "Bourke",
          "suburb" : "Melbourne",
          "state" : "Victoria",
          "country" : "Australia",
          "postcode" : "3000"
       },
       "phoneContact" : {
          "work" : "(03) 9663 3554",
          "home" : "(03) 9663 3554",
          "mobile" : "0411 888 000"
       },
       "fax" : "(03) 9663 3555",
       "emailAddress" : "alfred.sample@example.com",
       "dob" : "1995-12-08",
       "accountType" : 1,
       "accountTerms" : 1,
       "custom" : {
          "sms_subscribe" : false,
          "referrer" : "Acme Telecoms"
       }
    }

Account attributes
------------------

====================== =========== =================================================================================== =============
Field name             Data type   Description                                                                         Required?
====================== =========== =================================================================================== =============
accountTerms           Number      Acterms ID from Smile. 
                                   
releaseDelay           Number      
taxable                Boolean     
comments               String
tradingName            String
abn                    String
companyName            String
contactTitle           String
givenName              String
familyName             String
emailAddress           String
serviceAddress         Json object For more information, see :ref:`serviceAddress attributes`.
billAddress            Json object For more information, see :ref:`billAddress attributes`.
phoneContact           Json object For more information, see :ref:`phoneContact attributes`.
fax                    String
dob                    String      Format: yyyy-MM-dd 
                                   
                                   For example: 2017-11-16
                                   
accountType            Number      Account type from Smile.
custom                 Json object Data is in code/value pairs. Value can be an object or array.
                                   
                                   For example:                                    
                                   {"test_text":"value","is_bool":true,"test_date": “2018-12-08”,”test_number":
                                   123.45, “note”: [“Important note1”, “Important note2”]}
                                   
                                   **Note**: Date must be in yyyy-MM-dd format. If there is no matching custom 
                                   field from provided code in Smile, a new one will be created.
====================== =========== =================================================================================== =============

.. _serviceAddress attributes:

serviceAddress attributes
-------------------------

============= ========= ============================================================================ =========
Field name    Data type Description                                                                  Required?
============= ========= ============================================================================ =========
addressDetail String
streetNumber  String
streetName    String
streetType    String    Allowed values: "select code,name from addressLookup where lookupType = 0;”.
                        
                        Can be code or name.
suburb        String
postcode      String
state         String    Allowed values: "select code,name from addressLookup where lookupType = 1;”.
                        
                        Can be code or name.
country       String
============= ========= ============================================================================ =========

.. _billAddress attributes:

billAddress attributes
----------------------

============= ========= ============================================================================== =========
Field name    Data type Description                                                                    Required?
============= ========= ============================================================================== =========
addressDetail String
streetNumber  String
streetName    String
streetType    String    Allowable values: "select code,name from addressLookup where lookupType = 0;”. 
                        
                        Can be code or name.
suburb        String
postcode      String
state         String    Allowed values: "select code,name from addressLookup where lookupType = 1;”. 
                        
                        Can be code or name.
country       String
============= ========= ============================================================================== =========

.. _phoneContact attributes:

phoneContact attributes
-----------------------

========== ========= =========== =========
Field name Data type Description Required?
========== ========= =========== =========
work       String
home       String
mobile     String
========== ========= =========== =========

Success Response
================
This request returns an account ID updated and status.

Example:
--------

**Code:** 200 (OK)

**Content:** ::

    {
      “accountId”:"e5f946bb-6b31-4bbd-ae6c-247c54a57b4b",
      “status":"UPDATED"
    }

Error Response
==============

Example:
--------
**Code:** 500 (Internal Server Error)

**Description:** Returned if something fails during an update. You can find more details from the server’s log.

**Content:** ::

   {
     “accountId":"e5f946bb-6b31-4bbd-ae6c-247c54a57b4b",
     “status":"INTERNAL_ERROR"
   }

Example:
--------
**Code:** 200

* ``NOT_ACCOUNT``
* ``ACCOUNT_MISSING``
* ``TIMEZONE_NOT_FOUND``
* ``ACCOUNT_TYPE_NOT_FOUND``

**Content:** ::

    {
      “accountId":"e5f946bb-6b31-4bbd-ae6c-247c54a57b4b",
      “status":"ERROR",
      “errors":[
        “NOT_ACCOUNT",
        "TIMEZONE_NOT_FOUND"
      ]
    }

Sample Call
=========== 
::

    POST /api/account HTTP/1.1
    URL: https://smile.example.com/test/api/account/e5f946bb-6b31-4bbd-ae6c-247c54a57b4b/update
    Content-Type:application/json
    Accept:application/json    
                    
    {
       "taxable" : true,
       "releaseDelay" : 0,
       "comments" : "Comments",
       "contactTitle" : "MR",
       "givenName" : "Alfred",
       "familyName" : "Sample",
       "abn" : "94 088 172 301",
       "serviceAddress" : {
          "addressDetail" : "Main Building",
          "streetNumber" : "120",
          "streetType" : "Road",
          "streetName" : "Main",
          "suburb" : "Melbourne",
          "country" : "Australia",
          "postcode" : "3000"
       },
       "companyName" : "Example Telecom",
       "tradingName" : "Example Telco",
       "billAddress" : {
          "streetNumber" : "620",
          "streetType" : "Street",
          "streetName" : "Bourke",
          "suburb" : "Melbourne",
          "state" : "Victoria",
          "country" : "Australia",
          "postcode" : "3000"
       },
       "phoneContact" : {
          "work" : "(03) 9663 3554",
          "home" : "(03) 9663 3554",
          "mobile" : "0411 888 000"
       }, 
       "fax" : "(03) 9663 3555",
       "emailAddress" : "alfred.sample@example.com",
       "dob" : "1995-12-08",
       "accountType" : 1,
       "accountTerms" : 1,
       "custom" : {
          "sms_subscribe" : false,
          "referrer" : "Acme Telecoms"
       }
    }
