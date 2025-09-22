*************************
v3.0.x (X, X, 2025)
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



Contributors
------------
* Chris Deline (:ghuser:`cdeline`)

