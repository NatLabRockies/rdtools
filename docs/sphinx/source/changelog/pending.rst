***************
Pending Changes
***************


Maintenance
-----------
* Replaced the lowercase ``'d'`` offset alias, which pandas 3.0 deprecates,
  with ``'D'`` in ``Timedelta`` and rolling-window strings, including the
  default ``k`` of :py:func:`~rdtools.filtering.hampel_filter`. (:pull:`522`)

Testing
-------
* ``test_avg_timestamp_old_Pandas`` takes the expected datetime resolution
  from ``pd.to_datetime(..., unit='s')``, which returns microseconds from
  pandas 3.1. (:pull:`522`)

Contributors
------------
* :ghuser:`maoji-y`
