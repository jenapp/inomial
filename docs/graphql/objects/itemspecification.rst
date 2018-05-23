.. _itemspecification:

ItemSpecification
=================
Item Description

::

  type ItemSpecification {
  
    itemSpecification: Int

    itemCode: String

    name: String

    reportingAccount: Int

    quantityDivisor: Int

    quantityFormat: String

    displayRate: String

    displayOrder: Int

    taxable: Boolean

    taxSummaryItem: Boolean

    quantityType: Int

    defaultRate: BigDecimal

    currency: String

    taxTreatment: Int

    custom: String
  }

Required by
-----------
:ref:`allinvoiceitemcursor`
  *AllInvoiceItemCursor*
:ref:`txitem`
  *Transaction line item*
