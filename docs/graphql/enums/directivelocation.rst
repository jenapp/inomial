.. _directivelocation:

__DirectiveLocation
===================

An enum describing valid locations where a directive can be placed.

::

  enum __DirectiveLocation {
  
    # Indicates the directive is valid on queries.
    QUERY
    
    # Indicates the directive is valid on mutations.
    MUTATION
    
    # Indicates the directive is valid on fields.
    FIELD
    # Indicates the directive is valid on fragment definitions.
    FRAGMENT_DEFINITION
    
    # Indicates the directive is valid on fragment spreads.
    FRAGMENT_SPREAD
    
    # Indicates the directive is valid on inline fragments.
    INLINE_FRAGMENT
    
    # Indicates the directive is valid on a schema IDL definition.
    SCHEMA
    
    # Indicates the directive is valid on a scalar IDL definition.
    SCALAR
    
    # Indicates the directive is valid on an object IDL definition.
    OBJECT
    
    # Indicates the directive is valid on a field IDL definition.
    FIELD_DEFINITION
    
    # Indicates the directive is valid on a field argument IDL definition.
    ARGUMENT_DEFINITION
    
    # Indicates the directive is valid on an interface IDL definition.
    INTERFACE
    
    # Indicates the directive is valid on an union IDL definition.
    UNION
    
    # Indicates the directive is valid on an enum IDL definition.
    ENUM
    
    # Indicates the directive is valid on an input object IDL definition.
    INPUT_OBJECT
    
    # Indicates the directive is valid on an input object field IDL definition.
    INPUT_FIELD_DEFINITION
  }


Required by
-----------

:ref:`directive`
   *null*
