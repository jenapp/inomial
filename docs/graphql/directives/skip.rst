.. _skip:

skip
====

Directs the executor to skip this field or fragment when the ``if`` argument is true.

::
  
  directive @skip(if: Boolean!) on FIELD | FRAGMENT_SPREAD | INLINE_FRAGMENT

Required by
-----------

This element is not required
