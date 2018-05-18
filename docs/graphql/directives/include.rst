include
=======

Directs the executor to include this field or fragment only when the ``if`` argument is true.

::

  directive @include(if: Boolean!) on FIELD | FRAGMENT_SPREAD | INLINE_FRAGMENT


Required by
-----------

This element is not required
