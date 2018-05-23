.. _txfilter:

TxFilter
=========
::

  input TxFilter {
  
    tx: Long

    txUuid: UUID

    txDetail: Long

    account: Long

    txType: Int

    txNumber: String

    ledgerDate: String

    ledgerTime: Milliseconds

    currency: String

    amount: BigDecimal

    taxAmount: BigDecimal

    unallocatedAmount: BigDecimal

    creatingOperator: Int

    creationTime: Milliseconds

    comments: String

    reportingAccount: Int

    paymentPlan: Int

    txDisposition: Int

    referencedTx: Int

    documentType: Int

    stationery: Int
  }

Required by
------------
:ref:`account`
  *A debtor record containing transactions*
