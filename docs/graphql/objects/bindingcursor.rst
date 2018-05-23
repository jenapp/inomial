.. _bindingcursor:

BindingCursor
=============

::

  type BindingCursor {
  
    count: Int

    # Arguments
    # offset: [Not documented]
    # limit: [Not documented]
    objects(offset: Int, limit: Int): [Binding]
  }

Required by
-----------
:ref:`account`
  *A debtor record containing transactions*
