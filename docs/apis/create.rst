======
create
======
The create REST API posts a structured JSON document to create accounts and services.

URL
===

``https://smile.example.com/stage/api/orders``

Method
======
POST

URL Params
==========
No URL params exist for this request.

Document Format
===============
**Example:** ::

    {
       "accounts" : [
          {
             "taxable" : true,
             "packageId" : 27,
             "comments" : "Comments",
             "fax" : "(03) 9663 3555",
             "ratingCycleDay" : 31,
             "invoicingCycleDay" : 31,
             "phoneContact" : {
                "work" : "(03) 9663 3554",
                "home" : "(03) 9663 3554",
                "mobile" : "0411 888 000"
             },
             "releaseDelay" : 0,
             "contactTitle" : "MR",
             "givenName" : "John",
             "familyName" : "Smith",
             "abn" : "94 088 172 301",
             "serviceAddress" : {
                "country" : "Australia",
                "postcode" : "3000",
                "suburb" : "Melbourne",
                "streetNumber" : "120",
                "streetType" : "Road",
                "streetName" : "Main",
                "addressDetail" : "Main Building",
                "state" : "Victoria"
             },
             "companyName" : "Example Telecom",
             "billAddress" : {
                "streetNumber" : "620",
                "streetType" : "Street",
                "streetName" : "Bourke",
                "country" : "Australia",
                "suburb" : "Melbourne",
                "state" : "Victoria",
                "postcode" : "3000"
             },
             "timezone" : "Australia/Victoria",
             "alternateAccountNumber" : "abc111115",
             "currency" : "AUD",
             "tradingName" : "Example Telco",
             "emailAddress" : "john.smith@example.com",
             "dob":"1995-12-08"
             "custom" : {
                "sms_subscribe" : false,
                "referrer" : "Acme Telecoms"
             }
          }
       ],
       "subscriptions" : [
          {
             "releaseDelay" : 0,
             "startTime" : 1514725200000,
             "description" : "The A2 Start D Plan",
             "plan" : "a2startd",
             "username" : "john.adsl@example.com",
             "currency" : "AUD",
             "ratingCycleDay" : 31,
             "invoicingCycleDay" : 31,
             "timezone" : "Australia/Victoria",
             "serviceId" : 382,
             "custom" : {
                "newsletter_subscribe" : true,
                "productDescription" : "3G Wireless Modem",
                "productCode" : "3gwifi",
                "colour" : "Purple"
             }
          }
       ]
    }

Account attributes
------------------

====================== =========== =================================================================================== =============
Field name             Data type   Description                                                                         Required?
====================== =========== =================================================================================== =============
USN                    String
alternateAccountNumber String      AccountID from old system.

                                   Will be searchable in Smile and can be 
                                   used for linking to the other import files.
ratingCycleDay         Number      Default is the service’s period day or the company’s period day if 
                                   there is no service’s period day. 
                                   
                                   Default is 31 when there is no service’s period day or company’s period day.
invoicingCycleDay      Number      Default is the service’s invoicing day or the company’s invoicing day if 
                                   there is no service’s invoicing day.
                                   
                                   Default is 31 when there is no service’s invoicing day or company’s invoicing day.
releaseDelay           Number      Default is company’s release delay
currency               String      Currency from Smile. 
                                   
                                   The three letter ISO 4217 currency code of the payment amount. 
                                   
                                   For example: AUD, USD, FJD. 
                                   
                                   Default is package's currency.
accountTerms           Number      Acterms ID from Smile. 
                                   
                                   Default is package’s account terms.
taxable                Boolean     Default is True
packageId              Number      Package ID from Smile                                                               Yes
comments               String
tradingName            String
abn                    String
companyName            String
contactTitle           String
givenName              String
familyName             String
emailAddress           String
serviceAddress         Json object For more information, see `serviceAddress attributes`_.
billAddress            Json object For more information, see `billAddress attributes`_.
phoneContact           Json object For more information, see `phoneContact attributes`_.
fax                    String
timezone               String      Full time zone name. 
                                   
                                   For example: Australia/Adelaide. 
                                   
                                   Timezone’s default will be company’s timezone
dob                    String      Format: yyyy-MM-dd 
                                   
                                   For example: 2017-11-16
custom                 Json object Data is in code/value pairs. 
                                   
                                   For example: {"test\_text":"value","is\_bool":true,"test\_date": "2018-12-08",
                                   "test\_number":123.45} 
                                   
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

Subscription attributes
-----------------------

================== =========== ===================================================================================================== ==================================
Field name         Data type   Description                                                                                           Required?
================== =========== ===================================================================================================== ==================================
accountId                      Account UUID from Smile                                                                               Yes (if has no account in request)
serviceId                      Service ID from Smile                                                                                 Yes
username           String
plan               String      Plan ID from Smile
startTime  Number      Time in milliseconds since the UNIX epoch (January 1, 1970 00:00:00 UTC) 
                               
                               For example: 1514725200000
timezone           String      Full time zone name. 
                               
                               For example: Australia/Adelaide. 
                               
                               Default is inherited from account.
description        String
ratingCycleDay     Number      Default is inherited from account
invoicingCycleDay  Number      Default is inherited from account
releaseDelay       Number      Default is inherited from account
currency           String      Currency from Smile. 
                               
                               The three letter ISO 4217 currency code of the payment amount. 
                               
                               For example: AUD, USD, FJD. 
                               
                               Default is inherited from account.
custom             Json object Data is in code/value pairs. 
                               
                               For example: {"test\_text":"value","is\_bool":true,"test\_date": "2018-12-08","test\_number":123.45}
                               
                               **Note**: Date must be in yyyy-MM-dd format. 
                               If there is no matching custom field from provided code in Smile, a new one will be created.
================== =========== ===================================================================================================== ==================================

Success Response
================
This request returns a list of account UUID created and a list of subscription UUID created.

**Note**: Only 1 account create is supported.

Example:
--------

**Code:** 200 (OK)

**Content:** ::

    {
       "accounts" : {
          "0" : {
             "uuid" : "25f17058-35dd-4647-a00b-536c915c83cf"
          }
       },
       "subscriptions" : {
          "0" : {
             "uuid" : "dc120f6c-8c29-4e18-9944-c3b082ee1daa"
          },
          "1" : {
             "uuid" : "e0d540b7-5f3c-4c4f-a022-8447dfcba5df"
          }
       }
    }           

Error Response
==============

Example:
--------
**Code:** 500 (Internal Server Error)

**Description:** Returned if an import of more than one account or more than 100 subscriptions is attempted.

**Content:** Not applicable.

Example:
--------
**Code:** 200

* ``CURRENCY_NOT_AVAILABLE``
* ``CURRENCY_NOT_FOUND``
* ``PACKAGE_NOT_PUBLISHED``
* ``PACKAGE_NOT_FOUND``
* ``PACKAGE_MISSING``
* ``NO_PACKAGE_FOR_CURRENCY``
* ``SERVICE_NOT_PUBLISHED``
* ``SERVICE_NOT_FOUND``
* ``SERVICE_NOT_VALID``
* ``SERVICE_MISSING``
* ``PLAN_NOT_FOUND``
* ``PLAN_NOT_PUBLISHED``
* ``PLAN_NOT_VALID``
* ``NO_PLAN_FOR_SERVICE``
* ``NO_PLAN_FOR_ACCOUNT``
* ``NOT_ACCOUNT``
* ``ACCOUNT_MISSING``
* ``TIMEZONE_NOT_FOUND``
* ``DUPLICATE_USERNAME``
* ``DUPLICATE_LEGACY_ACCOUNT_NUMBER``
* ``INTERNAL_ERROR``

**Content:** ::

    {
       "accounts" : {
          "0" : {
             "errors" : [
                "CURRENCY_NOT_FOUND",
                "PACKAGE_NOT_FOUND"
             ]
          }
       },
       "subscriptions" : {
          "0" : {
             "errors" : [
                "NOT_ACCOUNT",
                "CURRENCY_NOT_FOUND",
                "SERVICE_NOT_FOUND",
                "PLAN_NOT_FOUND"
             ]
          },
          "1" : {
             "errors" : [
                "NOT_ACCOUNT",
                "CURRENCY_NOT_FOUND",
                "SERVICE_NOT_FOUND",
                "PLAN_NOT_FOUND"
             ]
          }
       }
    }

Sample Call
=========== 
::

    POST /api/orders HTTP/1.1
    URL: https://smile.example.com/test/api/orders
    Content-Type:application/json
    Accept:application/json    
                    
    {
       "accounts" : [
          {
             "taxable" : true,
             "packageId" : 27,
             "comments" : "Comments",
             "fax" : "(03) 9663 3555",
             "ratingCycleDay" : 31,
             "invoicingCycleDay" : 31,
             "phoneContact" : {
                "work" : "(03) 9663 3554",
                "home" : "(03) 9663 3554",
                "mobile" : "0411 888 000"
             },
             "releaseDelay" : 0,
             "contactTitle" : "MR",
             "givenName" : "John",
             "familyName" : "Smith",
             "abn" : "94 088 172 301",
             "serviceAddress" : {
                "country" : "Australia",
                "postcode" : "3000",
                "suburb" : "Melbourne",
                "streetNumber" : "120",
                "streetType" : "Road",
                "streetName" : "Main",
                "addressDetail" : "Main Building",
                "state" : "Victoria"
             },
             "companyName" : "Example Telecom",
             "billAddress" : {
                "streetNumber" : "620",
                "streetType" : "Street",
                "streetName" : "Bourke",
                "country" : "Australia",
                "suburb" : "Melbourne",
                "state" : "Victoria",
                "postcode" : "3000"
             },
             "timezone" : "Australia/Victoria",
             "alternateAccountNumber" : "abc111115",
             "currency" : "AUD",
             "tradingName" : "Example Telco",
             "emailAddress" : "john.smith@example.com",
             "dob":"1995-12-08"
             "custom" : {
                "sms_subscribe" : false,
                "referrer" : "Acme Telecoms"
             }
          }
       ],
       "subscriptions" : [
          {
             "releaseDelay" : 0,
             "startTime" : 1514725200000,
             "description" : "The A2 Start D Plan",
             "plan" : "a2startd",
             "username" : "john.adsl@example.com",
             "currency" : "AUD",
             "ratingCycleDay" : 31,
             "invoicingCycleDay" : 31,
             "timezone" : "Australia/Victoria",
             "serviceId" : 382,
             "custom" : {
                "newsletter_subscribe" : true,
                "productDescription" : "3G Wireless Modem",
                "productCode" : "3gwifi",
                "colour" : "Purple"
             }
          }
       ]
