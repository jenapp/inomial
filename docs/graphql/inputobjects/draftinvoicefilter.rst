.. _draftinvoicefilter:

DraftInvoiceFilter
==================
DraftInvoiceFilter

::

  input DraftInvoiceFilter {
  
    txdetailUuid: UUID

    txDetail: Int

    number: String

    account: Int

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
-----------
:ref:`query`
  *Smile's GraphQL Query type*
