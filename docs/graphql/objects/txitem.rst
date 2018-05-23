.. _txitem:

TxItem
======
Transaction line item

::

  type TxItem {
  
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

    # Arguments
    # filter: [Not documented]
    Subscription(filter: [SubscriptionFilter]): Subscription

    # Arguments
    # filter: [Not documented]
    Binding(filter: [BindingFilter]): Binding

    # Arguments
    # filter: [Not documented]
    CostCentre(filter: [AccountCostCentreFilter]): AccountCostCentre

    # Arguments
    # filter: [Not documented]
    ItemSpecification(filter: [ItemSpecificationFilter]): ItemSpecification
  }

Required by
-----------
:ref:`txitemcursor`
  *null*
