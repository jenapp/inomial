.. _subscriptionbindingfilter:

SubscriptionBindingFilter
=========================

::

  input SubscriptionBindingFilter {
  
    tid: Int

    subscriptionUuid: UUID

    bindingUuid: UUID

    startTime: Milliseconds

    endTime: Milliseconds

    timezone: Int

    active: Boolean
  }

Required by
------------
:ref:`binding`
  *Account's binding*
:ref:`subscription`
  *A subscription to a service*
