.. _subscriptionbinding:

SubscriptionBinding
===================
Subscription's binding

::

  type SubscriptionBinding {
  
    tid: Int

    subscriptionUuid: UUID

    bindingUuid: UUID

    startTime_iso: String

    startTime: Milliseconds

    endTime_iso: String

    endTime: Milliseconds

    timezone: Int

    active: Boolean

    # Arguments
    # filter: [Not documented]
    Binding(filter: [BindingFilter]): Binding
  }

Required by
-----------
:ref:`subscriptionbindingcursor`
  *null*
