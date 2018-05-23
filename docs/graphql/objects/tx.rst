.. _tx:

Tx
==
Information about a credit or debit that has been applied to an Account

::

  type Tx {
  
    tx: Long

    txUuid: UUID

    txDetail: Long

    account: Long

    txType: Int

    txNumber: String

    ledgerDate: String

    ledgerTime_iso: String

    ledgerTime: Milliseconds

    currency: String

    amount: BigDecimal

    taxAmount: BigDecimal

    unallocatedAmount: BigDecimal

    creatingOperator: Int

    creationTime_iso: String

    creationTime: Milliseconds

    comments: String

    reportingAccount: Int

    paymentPlan: Int

    txDisposition: Int

    referencedTx: Int

    documentType: Int

    stationery: Int

    # Arguments
    # filter: [Not documented]
    TxDetail(filter: [TxDetailFilter]): TxDetail

    # Arguments
    # filter: [Not documented]
    Account(filter: [AccountFilter]): Account

    # Arguments
    # filter: [Not documented]
    TxItems(filter: [TxItemFilter]): TxItemCursor
  }

Required by
-----------
:ref:`account`
  *A debtor record containing transactions*
:ref:`query`
  *Smile's GraphQL Query type*
