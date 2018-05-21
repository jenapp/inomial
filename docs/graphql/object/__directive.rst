__Directive
===========

::

  type __Directive {
  
      name: String
      
      description: String
      
      locations: [__DirectiveLocation!]
      
      args: [__InputValue!]!
      
      onOperation: Boolean @deprecated( reason: "Use `locations`." )
      
      onFragment: Boolean @deprecated( reason: "Use `locations`." )
      
      onField: Boolean @deprecated( reason: "Use `locations`." )
  }


Required by
-----------
__SchemaA
   GraphQL Introspection defines the capabilities of a GraphQL server. It exposes all available types and dire
