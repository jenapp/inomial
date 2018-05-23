.. _draftinvoice:

DraftInvoice
============
Draft invoice

::

  type DraftInvoice {
  
    txdetailUuid: UUID

    txDetail: Int

    number: String

    account: Int

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
:ref:`alldraftinvoicecursor`
  *AllDraftInvoiceCursor*
:ref:`query`
  *Smile's GraphQL Query type*
