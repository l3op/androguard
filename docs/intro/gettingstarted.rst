Getting Started
===============

The easiest way to analyze APK files, is by using :code:`androlyze.py`.
It will start a iPython shell and has all modules loaded to get into action.

Open a terminal and type :code:`androlyze.py -s`.

For analyzing and loading APK or DEX files, some wrapper functions exists.
Use :code:`AnalyzeAPK(filename)` or :code:`AnalyzeDEX(filename)` to load a file and start analyzing:

.. code-block:: python

    a, d, dx = AnalyzeAPK("/home/user/some-app.apk")

The three objects you get are :code:`a` an :class:`androguard.core.bytecodes.apk.APK` object, :code:`d` an array of :class:`androguard.core.bytecodes.dvm.DalvikVMFormat` object and :code:`dx` an :class:`androguard.core.analysis.analysis.Analysis` object.

Inside the :code:`APK` object, you can find all information about the APK, like package name, permissions, the AndroidManifest.xml
or its resources.

The :class:`androguard.core.bytecodes.dvm.DalvikVMFormat` corresponds to the DEX file found inside the APK file. You can get classes, methods or strings from
the DEX file.

The :class:`androguard.core.analysis.analysis.Analysis` object contains special classes, which link information about the classes.dex.
