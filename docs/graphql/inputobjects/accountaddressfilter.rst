.. _accountaddressfilter:

AccountAddressFilter
====================

::

  input AccountAddressFilter {
  
    account: Int

    addressType: Int

    addressName: String

    companyName: String

    addressDetail: String

    buildingName: String

    subUnit: String

    floor: String

    lot: String

    postalDeliveryType: String

    streetNumber: String

    streetName: String

    streetType: String

    suburb: String

    state: String

    postcode: String

    country: String
  }

Required by
-----------
:ref:`account`
  *A debtor record containing transactions*
