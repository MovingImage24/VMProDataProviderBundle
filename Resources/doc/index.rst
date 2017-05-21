Getting started with the VMPro Data Provider Bundle
===================================================

This Symfony bundle allows you to abstract away the need to interact directly with the Video
Manager Pro API together with the Video Collection bundle

Prerequisites
-------------

This bundle requires version 2.7+ or 3.0+ of the Symfony framework, and supports
PHP 5.6, 7.0 and 7.1, and will leverage any Guzzle library you already have installed into
your project, or if you don't have one, retrieve Guzzle 6.

Installation
------------

Installing this bundle is a quick and simple process that should only take a minute.

Install library with composer
_____________________________

First you have to install it using Composer:

.. code-block:: bash

    $ composer require movingimage/vmpro-data-provider-bundle

Enable bundle
_____________

Enable the bundle in your kernel:

.. code-block:: php

    <?php
    // app/AppKernel.php

    // ...
    class AppKernel extends Kernel
    {
        public function registerBundles()
        {
            $bundles = array(
                // ...

                new MovingImage\Bundle\DataProvider\VideoManagerPro\VMProDataProviderBundle(),
            );

            // ...
        }

        // ...
    }

Getting Started
_______________

After successful installation, you may use the data provider in your collections:

.. code-block:: yaml

    # app/config/configuration.yml

    video_collection:
        collections:
            video_list:
                data_provider: vmpro
                channel_id: 10110