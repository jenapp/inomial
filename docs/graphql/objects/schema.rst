.. _schema:

__Schema
========
A GraphQL Introspection defines the capabilities of a GraphQL server. It exposes all available types and directives on the server, the entry points for query, mutation, and subscription operations.

::

  type __Schema {
    
    # A list of all types supported by this server.
    types: [__Type!]!
    
    # The type that query operations will be rooted at.
    queryType: __Type!
    
    # If this server supports mutation, the type that mutation operations will be
    # rooted at.
    mutationType: __Type
    
    # 'A list of all directives supported by this server.
    directives: [__Directive!]!
    
    # 'If this server support subscription, the type that subscription operations will
    # be rooted at.
    subscriptionType: __Type
  }


Required by
-----------

This element is not required
