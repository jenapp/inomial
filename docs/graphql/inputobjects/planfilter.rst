.. _planfilter:

PlanFilter
==========
PlanFilter

::

  input PlanFilter {
  
    plan: String

    service: Int

    name: String

    userDescription: String

    operatorDescription: String

    isSuspensionPlan: Boolean

    firstAvailableDate: String

    lastAvailableDate: String

    custom: String
  }

Required by
-----------
:ref:`query`
  *Smile's GraphQL Query type*
