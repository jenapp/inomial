.. _txitemcursor:

TxItemCursor
============

::

  type TxItemCursor {
  
    count: Int

    # Arguments
    # offset: [Not documented]
    # limit: [Not documented]
    objects(offset: Int, limit: Int): [TxItem]
  }

Required by
------------
:ref:`draftinvoice`
  *Draft invoice*
:ref:`tx`
  *Information about a credit or debit that has been applied to an Account*
:ref:`txdetail`
  *Detailed information about a (possibly draft) transaction*
