.. _binding:

Binding
========
Account's binding

::

  type Binding {
  
    tid: Int

    bindingUuid: UUID

    accountUuid: UUID

    planUuid: UUID

    planName: String

    planCode: String

    startTime_iso: String

    startTime: Milliseconds

    endTime_iso: String

    endTime: Milliseconds

    cancelled: Boolean

    issueCycle: Int

    issueFrequency: Int

    chargeCycle: Int

    chargeFrequency: Int

    timezone: Int

    active: Boolean

    # Arguments
    # filter: [Not documented]
    SubscriptionBindings(filter: [SubscriptionBindingFilter]): SubscriptionBindingCursor
  }

Required by
------------
:ref:`bindingcursor`
  *null*
:ref:`subscriptionbinding`
  *Subscription's binding*
:ref:`txitem`
  *Transaction line item*
