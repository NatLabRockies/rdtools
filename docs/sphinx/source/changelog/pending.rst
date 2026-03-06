*******
Pending
*******

Maintenance
-----------
* Migrated project configuration from ``setup.py``/``setup.cfg`` to
  ``pyproject.toml`` using ``setuptools`` as the build backend.
  (:pull:`488`)
* Replaced ``versioneer`` with ``setuptools-scm`` for automatic version
  management from git tags. (:pull:`488`)
* Removed legacy build files: ``setup.py``, ``setup.cfg``, ``versioneer.py``,
  ``MANIFEST.in``, and ``rdtools/_version.py``. (:pull:`488`)
* Updated ``rdtools/__init__.py`` to use ``importlib.metadata`` for version
  retrieval instead of versioneer. (:pull:`488`)
* Updated GitHub URLs and references from ``NREL/rdtools`` to
  ``NatLabRockies/rdtools`` and email addresses from ``@nrel.gov`` to
  ``@nlr.gov``. (:pull:`492`)
* Adopted `pixi <https://pixi.sh>`_ for reproducible environment management.
  Replaced ``requirements.txt``, ``requirements-min.txt``, and
  ``docs/notebook_requirements.txt`` with pixi environments and a lockfile.
  (:pull:`492`)
* Rewrote CI workflows (``pytest.yaml``, ``nbval.yaml``) to use pixi via
  ``prefix-dev/setup-pixi`` and removed the ``requirements.yaml`` workflow.
  (:pull:`492`)
* Bumped minimum ``arch`` version from 5.0 to 5.6. (:pull:`492`)
* Added Python 3.14 to the test matrix and package classifiers.
  (:pull:`492`)
* Simplified pixi environments: ``core`` (bare), ``default`` (notebooks),
  ``dev`` (notebooks + test, alias for ``dev-py313``), ``dev-py310`` through
  ``dev-py314`` (full dev per Python version), and ``dev-min`` (minimum
  dependency versions). All shared environments pin Python 3.13.
  (:pull:`492`)
* Added composable pip extras: ``[notebooks]``, ``[test]``, ``[dev]``,
  ``[doc]``, and ``[all]``. (:pull:`492`)
* Updated documentation (README, Sphinx index, developer notes, and example
  notebook setup cells) for pixi and pip extras. (:pull:`492`)

Bug Fixes
---------
* Fixed broken link to TrendAnalysis example in Sphinx index page.
  (:pull:`492`)

Requirements
------------
* Bumped minimum ``xgboost`` version from 1.6.0 to 1.7.0 to fix
  ``pkg_resources`` import error in environments without ``setuptools``.
  (:pull:`493`)
* Bumped minimum ``pvlib`` version from 0.12.0 to 0.13.1 to include the
  ``detect_clearsky()`` bug fix (pvlib GH2550). (:pull:`493`)

