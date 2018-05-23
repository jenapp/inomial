.. _itemspecificationfilter:

ItemSpecificationFilter
=======================

::

  input ItemSpecificationFilter {
  
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
------------
:ref:`query`
  *Smile's GraphQL Query type*
:ref:`txitem`
  *Transaction line item*
