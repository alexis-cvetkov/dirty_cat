=================================================
dirty_cat: machine learning on dirty categories
=================================================

.. toctree::
   :maxdepth: 2

.. currentmodule:: dirty_cat

`dirty_cat` helps with machine-learning on
non-curated categories. It provides **encoders that are
robust to morphological variants**, such as typos, in the category strings.

The :class:`SimilarityEncoder` is a drop-in replacement for
`scikit-learn <https://scikit-learn.org>`_'s
:class:`~sklearn.preprocessing.OneHotEncoder`.
If speed and scalability are an issue, the :class:`MinHashEncoder` provides
a fast encoding method.

For a detailed description of the problem of encoding dirty categorical data,
see `Similarity encoding for learning with dirty categorical variables
<https://hal.inria.fr/hal-01806175>`_ [1]_ and `Encoding high-cardinality
string categorical variables <https://hal.inria.fr/hal-02171256v4>`_ [2]_.

:Installing: `$ pip install --user dirty_cat`

.. rst-class:: right-align

   `Recent changes <CHANGES.html>`_

*Requires Python 3*

______

.. include:: auto_examples/index.rst
    :start-line: 2
    :end-before: .. container:: sphx-glr-footer

API documentation
=================

Encoders
------------

.. autosummary::
   :toctree: generated/
   :template: class.rst
   :nosignatures:

   MinHashEncoder
   SimilarityEncoder
   TargetEncoder

Data download
-----------------------

.. autosummary::
   :toctree: generated/
   :template: function.rst
   :nosignatures:

   datasets.fetch_employee_salaries
   datasets.fetch_medical_charge
   datasets.fetch_midwest_survey
   datasets.fetch_open_payments
   datasets.fetch_road_safety
   datasets.fetch_traffic_violations
   datasets.get_data_dir

About
=========

dirty_cat is for now a repository for developing ideas with high-quality
implementations, a form of a research project: there is still
little known about the problems of dirty categories. We hope that
tradeoffs will emerge in the long run, and that these tradeoffs will
enable us to do better software. We really need people giving feedback on
success and failures with the different techniques and pointing us to
open datasets on which we can do more empirical work. We also welcome
contributions in the scope of dirty categories.


.. seealso::

   Many classic categorical encoding schemes are available here:
   http://contrib.scikit-learn.org/categorical-encoding/

   Similarity encoding in also available in Spark ML:
   https://github.com/rakutentech/spark-dirty-cat

.. [1] Patricio Cerda, Gaël Varoquaux, Balázs Kégl. Similarity encoding for learning with dirty categorical variables. 2018. Machine Learning journal, Springer.
.. [2] Patricio Cerda, Gaël Varoquaux. Encoding high-cardinality string categorical variables. 2020. IEEE Transactions on Knowledge & Data Engineering.

