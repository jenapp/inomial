.. _txdetailfilter:

TxDetailFilter
==============

::

  input TxDetailFilter {
  
    txdetailUuid: UUID

    txDetail: Long

    number: String

    account: Long

    ledgerTime: Milliseconds

    creationTime: Milliseconds

    closedDate: Milliseconds

    dueDate: Milliseconds

    amount: BigDecimal

    taxAmount: BigDecimal

    reportingAccount: Int

    comments: String

    version: Int

    discount: BigDecimal

    lateFeeTxItem: Int
  }

Required by
------------
:ref:`tx`
  *Information about a credit or debit that has been applied to an Account*
