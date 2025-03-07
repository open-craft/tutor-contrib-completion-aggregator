completion-aggregator plugin for `Tutor <https://docs.tutor.edly.io>`__
###############################################################################

This plugin is a companion to `tutor-contrib-aspects`_ which demonstrates how to extend Aspects to display non-standard tracking events.

See `openedx-aspects#222`_ for more details.

When enabled in Tutor, this plugin installs:

* OpenCraft's `openedx-completion-aggregator`_ platform plugin
* `dbt-completion-aggregator`_ dbt extension
* `custom Superset assets`_: dataset, dashboard, and charts

Installation
************

.. code-block:: bash

    pip install git+https://github.com/open-craft/tutor-contrib-completion-aggregator

Usage
*****

.. code-block:: bash

    # Enable this plugin
    tutor plugins enable completion-aggregator

    # Update config to use this plugin
    tutor config save

    # Rebuild openedx image to update pip dependencies
    tutor images build openedx

    # Run custom dbt
    tutor local do dbt -c "run"

    # Import and the assets added by this plugin
    tutor local do import-assets

License
*******

This software is licensed under the terms of the AGPLv3.


.. _openedx-aspects#222: https://github.com/openedx/openedx-aspects/issues/222
.. _tutor-contrib-aspects: https://github.com/openedx/tutor-contrib-aspects
.. _openedx-completion-aggregator: https://github.com/open-craft/openedx-completion-aggregator
.. _dbt-completion-aggregator: https://github.com/open-craft/dbt-completion-aggregator
.. _custom Superset assets: tutor_completion_aggregator/templates/superset-assets
