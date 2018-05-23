.. _txitemfilter:

TxItemFilter
============

::

  input TxItemFilter {
  
    txItem: Long

    txDetail: Long

    itemCode: String

    lineNumber: Int

    ratingPeriod: Int

    itemSpecification: Int

    taxDate: String

    taxDurationDays: Int

    description: String

    quantity: BigDecimal

    eventCount: Int

    displayRate: String

    generated: Boolean

    amount: BigDecimal

    subtotalAmount: BigDecimal

    subscriptionUuid: UUID

    taxSummaryItem: Boolean

    taxSchedule: Int

    tax: BigDecimal

    taxable: Boolean

    discount: Int

    discountAmount: BigDecimal

    purchaseOrder: UUID

    rollupTxItem: Int

    bindingUuid: UUID

    costCentre: Int
  }

Required by
-----------
:ref:`draftinvoice`
  *Draft invoice*
:ref:`tx`
  *Information about a credit or debit that has been applied to an Account*
:ref:`txdetail`
  *Detailed information about a (possibly draft) transaction*
