.. _section_options:

Options
=======

Nemesyst uses `ConfigArgParse <https://github.com/bw2/ConfigArgParse>`_ for argument handling.
This means you may pass in arguments as (in order of highest priority first):

* CLI arguments
* Environment variables
* ini format .conf config files
* Hard-coded defaults

In code Nemesyst will look for config files in the following default locations, in order of priority and with expansion (highest first):

.. literalinclude:: ../../nemesyst
    :pyobject: default_config_files

Using the --config argument you may specify more config files, which will be perpended to the default ones in the order supplied. Please note however config file locations are only followed once to avoid infinite loops where two configs point to each other, making Nemesyst read one then the other infinitely.

.. _section_all-options:

All Options by Category
***********************

.. argparse::
   :module: nemesyst
   :func: argument_parser
   :prog: nemesyst
