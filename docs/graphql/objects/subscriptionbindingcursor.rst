.. _subscriptionbindingcursor:

SubscriptionBindingCursor
=========================

::

  type SubscriptionBindingCursor {
  
    count: Int

    # Arguments
    # offset: [Not documented]
    # limit: [Not documented]
    objects(offset: Int, limit: Int): [SubscriptionBinding]
  }

Required by
------------
:ref:`binding`
  *Account's binding*
:ref:`subscription`
  *A subscription to a service*
