.. _paymentmethodfilter:

PaymentMethodFilter
===================

::

  input PaymentMethodFilter {
  
    tid: Int

    accountId: UUID

    paymentMethod: UUID

    hint: String

    expiryDate: String

    isDefault: Boolean
  }
  
Required by
-----------
:ref:`account`
  *A debtor record containing transactions*
