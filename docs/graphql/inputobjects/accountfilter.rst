.. _accountfilter:

AccountFilter
=============

::

  input AccountFilter {
  
    account: Long

    accountUuid: UUID

    usn: String

    alternateAccountNumber: String

    accountType: Int

    accountTerms: Int

    accountDisposition: Int

    discount: Int

    creationTime: Milliseconds

    accountCostCentre: Int

    description: String

    taxable: Boolean

    taxSchedule: Int

    currency: String

    timezone: Int

    uoobject: Int

    custom: String
  }


Required by
------------
:ref:`draftinvoice`
  *Draft invoice*
:ref:`query`
  *Smile's GraphQL Query type*
:ref:`subscription`
  *A subscription to a service*
:ref:`ticket`
  *Tickets (work orders)*
:ref:`tx`
  *Information about a credit or debit that has been applied to an Account*
:ref:`txdetail`
  *Detailed information about a (possibly draft) transaction*
