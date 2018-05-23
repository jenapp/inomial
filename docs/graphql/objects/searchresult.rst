.. _searchresult:

SearchResult
=============
A single result from a search query.

::

  type SearchResult {
  
    # Highest ranking match for this account.
    accountRank: Int!

    # Rank of this result within the account.
    resultRank: Int!

    # The type of this result.
    resultType: Int!

    # Debtor item ID for this result, if any
    debtorItem: Int

    # Account associated with this result
    account: Account!

    # Subscription associated with this result, if any
    sub: Subscription
  }

Required by
------------
:ref:`query`
  *Smile's GraphQL Query type*
