.. _accountcontact:

AccountContact
==============
Contact details for an account

::

  type AccountContact {
  
    account: Long

    contactType: Int

    contactName: String

    companyName: String

    tradingName: String

    abn: String

    contactTitle: String

    familyName: String

    givenName: String

    dateOfBirth: String

    gender: String

    position: String

    phoneHome: String

    phoneWork: String

    phoneMobile: String

    fax: String
  }

Required by
-----------
:ref:`account`
  *A debtor record containing transactions*
