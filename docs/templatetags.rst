.. _templatetags:

Template Tags
=============

reminders
---------

The `reminders` tag loops through the `REMINDERS` list of callables and
evaluates them for the current user (requires the request object to be
in context. If the callable returns a dict instead None, then it will
evaluate the message in the same tuple and add that to the results list.
After evaluating all callables it sets a context variable to the list::

    {% reminders as user_reminders %}
