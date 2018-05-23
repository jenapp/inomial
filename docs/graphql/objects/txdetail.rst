.. _txdetail:

TxDetail
========
Detailed information about a (possibly draft) transaction

::

  type TxDetail {
  
    txdetailUuid: UUID

    txDetail: Long

    number: String

    account: Long

    ledgerTime_iso: String

    ledgerTime: Milliseconds

    creationTime_iso: String

    creationTime: Milliseconds

    closedDate_iso: String

    closedDate: Milliseconds

    dueDate_iso: String

    dueDate: Milliseconds

    amount: BigDecimal

    taxAmount: BigDecimal

    reportingAccount: Int

    comments: String

    version: Int

    discount: BigDecimal

    lateFeeTxItem: Int

    # Arguments
    # filter: [Not documented]
    TxItems(filter: [TxItemFilter]): TxItemCursor

    # Arguments
    # filter: [Not documented]
    Account(filter: [AccountFilter]): Account
  }

Required by
-----------
:ref:`query`
  *Smile's GraphQL Query type*
:ref:`tx`
  *Information about a credit or debit that has been applied to an Account*
