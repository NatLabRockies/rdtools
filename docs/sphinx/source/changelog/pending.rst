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
