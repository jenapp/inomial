.. _paymentmethod:

PaymentMethod
=============
Saved payment details for an account

::

  type PaymentMethod {
  
    tid: Int

    accountId: UUID

    paymentMethod: UUID

    hint: String

    expiryDate: String

    isDefault: Boolean
  }

Required by
------------
:ref:`account`
  *A debtor record containing transactions*
