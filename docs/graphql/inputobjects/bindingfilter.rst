.. _bindingfilter:

BindingFilter
=============

::

  input BindingFilter {
  
    tid: Int

    bindingUuid: UUID

    accountUuid: UUID

    planUuid: UUID

    planName: String

    planCode: String

    startTime: Milliseconds

    endTime: Milliseconds

    cancelled: Boolean

    issueCycle: Int

    issueFrequency: Int

    chargeCycle: Int

    chargeFrequency: Int

    timezone: Int

    active: Boolean
  }

Required by
------------
:ref:`account`
  *A debtor record containing transactions*
:ref:`subscriptionbinding`
  *Subscription's binding*
:ref:`txitem`
  *Transaction line item*
