Parameters an Data Formatting
=============================

Parameters
----------

Outbreak.info local requires two parameter files for fully functionality

1. Website parameters
2. Bjorn parameters

Additonally, if the bjorn service is going to be used, there is one parameter that must be changed in the `docker-compose.yml <https://github.com/andersen-lab/outbreak.info/blob/master/docker-compose.yml>`_ file, located `here <https://github.com/andersen-lab/outbreak.info/blob/master/docker-compose.yml#L14>`_.

* Recommeneded use is to replace this line with the absolute path of the bjorn submodule 

The website parameter file is nameed **localConfig.json** and can be found under

.. code-block:: console

    /web/src/localConfig.json
    
.. list-table:: Parameters in Website Configuration
   :widths: 30 40 40
   :header-rows: 1

   * - Parameter Name
     - Parameter Type
     - Description
   * - localBuildName 
     - String
     - the title of the build and website
   * - siteUrl
     - String
     - the url at which the website will be deployed
   * - locationFocus
     - String (Opt.)
     - the location around which the data focuses
   * - pathToZipcodes
     - String (Opt.)
     - the relative path to the zipcode geojson file (REMOVE IF NO ZIPCODE INFORMATION)
   * - cores
     - Int
     - the number of cores to run bjorn with
   * - gaTracking
     - String
     - google analytics tracking placeholder
   * - zipcodeFocus
     - String (Opt.)
     - the area we have zipcodes for (REMOVE IF NO ZIPCODE INFORMATION)


.. list-table:: Parameters for Bjorn
   :widths: 30 40 40
   :header-rows: 1

   * - Parameter Name
     - Parameter Type
     - Description
   * -  
     - 
     - 
   * - 
     - 
     - 
   * - 
     - 
     - 
   * - 
     - 
     - 
   * - 
     - 
     - 
   * - 
     - 
     - 
   * - 
     - 
     - 
   * - 
     - 
     - 

Data Formatting
---------------

Sequencing Data Formatting
^^^^^^^^^^^^^^^^^^^^^^^^^^

If using the dockerized version of bjorn included in outbreak.info local, sequencing data
must be formatted in the style of the `Andersen Lab Repository <https://github.com/andersen-lab/HCoV-19-Genomics>`_.Specifically it must contain

.. code-block:: console

    /consensus_sequences

with **.fasta** consensus sequences and 

.. code-block:: console

    /metadata.csv
    
with metadata formated using the same template. The url to the repository must be specified in bjorn configuration file as discussed above.

Zipcode Data Formatting
^^^^^^^^^^^^^^^^^^^^^^^
If you would like to include zipcode information, include the parameter *zipcodeFocus* in the localConfig.json configuration file.

Choropleths using zipcode data are a new feature added to the outbreak.info local project. The data for this feature must be provided in a .geojson file in the same format as the example file `here <www.google.com>`_.




