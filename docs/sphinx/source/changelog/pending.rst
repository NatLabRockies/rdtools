*************************
v3.2.0 (X, X, 2026)
*************************

Enhancements
------------
* :py:func:`~rdtools.degradation.degradation_year_on_year` has new parameter ``label=``
  to return the calc_info['YoY_values'] as either right labeled (default), left or
  center labeled. (:issue:`459`)
* :py:func:`~rdtools.plotting.degradation_timeseries_plot` has new parameter ``label=``
  to allow the timeseries plot to have right labeling (default), center or left labeling.
  (:issue:`455`)
* :py:func:`~rdtools.degradation.degradation_year_on_year` has new parameter ``multi_yoy``
  (default False) to trigger multiple YoY degradation calculations similar to Hugo Quest et
  al 2023. In this mode, instead of a series of 1-year duration slopes, 2-year, 3-year etc
  slopes are also included.  calc_info['YoY_values'] returns a non-monotonic index
  in this mode due to multiple overlapping annual slopes.  (:issue:`394`)
* :py:func:`~rdtools.plotting.degradation_timeseries_plot` now supports ``multi_yoy=True``
  data by resampling overlapping YoY values to their mean. A warning is issued when this
  resampling occurs.  (:issue:`394`)
* :py:func:`~rdtools.plotting.degradation_summary_plots` ``detailed=True`` mode now
  properly handles points used odd vs even number of times (not just 0, 1, 2).
  (:issue:`394`)

Testing
-------
* Added tests for error handling paths in :py:mod:`~rdtools.analysis_chains`:
  ``filter_params`` and ``filter_params_aggregated`` setter validation,
  ``clearsky_rescale_index_mismatch``, ``poa_filter_without_poa``,
  ``tcell_filter_without_temperature``, ``hour_angle_filter_without_location``,
  ``clearsky_filter_without_poa``, and ``degradation_timeseries_plot_invalid_case``.
* Added tests for error handling paths in :py:mod:`~rdtools.degradation`:
  ``classical_decomposition`` missing/irregular data, ``year_on_year`` circular block
  validation, no valid pairs error, and ``_mk_test`` edge cases (no trend, ties,
  decreasing).
* Set matplotlib backend to ``Agg`` in test ``conftest.py`` to avoid tkinter issues.


Contributors
------------
* Chris Deline (:ghuser:`cdeline`)
* Martin Springer (:ghuser:`martin-springer`)

