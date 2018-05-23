.. _Type:

__Type
======

::


  type __Type {
  
    kind: __TypeKind!
    
    name: String
    
    description: String
    
    # Arguments
    # includeDeprecated: [Not documented]
    fields(includeDeprecated: Boolean): [__Field!]
    
    interfaces: [__Type!]
    
    possibleTypes: [__Type!]
    
    # Arguments
    # includeDeprecated: [Not documented]
    enumValues(includeDeprecated: Boolean): [__EnumValue!]
    
    inputFields: [__InputValue!]
    
    ofType: __Type
  }


Required by
-----------

:ref:`Field`
   *null*
:ref:`InputValue`
   *null*
:ref:`Schema`
   *A GraphQL Introspection defines the capabilities of a GraphQL server. It exposes all available types and directives on the server, the entry points for query, mutation, and subscription operations.*
:ref:`Type`
   *null*
