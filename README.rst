==============
 AWS-Datapipe
==============

A tool for creating AWS data pipeline. Currently only for **exporting data from any DynamoDB table to an existing S3 bucket** 
and store the Pipeline Definition as a backup. New features are going to be added (check for updates).

`Just because terraform can't do it yet..`

---------------
 Prerequisites
---------------

**This tool supports only Python 3 because Python 2.7 will not be maintained past 2020**

AWS-Datapipe uses awscli to configure pipelines in your AWS account. By default, installing aws-datapipe you will also
install all the prerequisites, so you can skip this phase and move to the `Installation step`. But in case if you want to do it manually:

The easiest way to install aws-cli is to use `pip <https://pypi.org/project/pip/>`_ in a ``virtualenv``::

    $ pip install awscli

or, if you are not installing in a ``virtualenv``, to install globally::

    $ sudo pip install awscli

or for your user::

    $ pip install --user awscli

If you have the aws-cli installed and want to upgrade to the latest version
you can run::

    $ pip install --upgrade awscli

Because aws-datapipe is based on aws-cli, before using aws-datapipe, 
you need to configure your AWS credentials using aws-cli.  
You can do this in several ways:

* Environment variables
* Shared credentials file
* Config file
* IAM Role

The quickest way to get started is to run the ``aws configure`` command::

    $ aws configure
    AWS Access Key ID: foo
    AWS Secret Access Key: bar
    Default region name [us-west-2]: us-west-2
    Default output format [None]: json

For additional info and other ways of aws-cli configuration you can check `here <https://docs.aws.amazon.com/cli/latest/userguide/cli-chap-configure.html>`_

---------------
 Installing
---------------

The easiest way to install aws-datapipe is to use `pip <https://pypi.org/project/pip/>`_ in a ``virtualenv``::

    $ pip install aws-datapipe

or, if you are not installing in a ``virtualenv``, to install globally::

    $ sudo pip install aws-datapipe

or for your user::

    $ pip install --user aws-datapipe

If you have the aws-datapipe installed and want to upgrade to the latest version
you can run::

    $ pip install --upgrade aws-datapipe


End with an example of getting some data out of the system or using it for a little demo

---------------
Getting Started
---------------
You can use AWS Datapipe in two different ways: 

* interactive
* passing arguments

To list all available arguments and additional info check please the ``--help``.

For interactive mode just start the tool ``aws-datapipe`` and it will ask you for the required information to build a pipeline.

After creating data pipeline in AWS, datapipe will save locally a `pipeline definition file` with the same name as your 
pipeline that can be used as a backup. After that you can activate the pipeline directly in the script on the next step:

``Would you like to activate the pipeline now? [y/n]``  

You can omit activation and manually activate the pipeline later whenever you want from the AWS Console

Currently ``aws-datapipe`` is creating pipeline which will **run every 14 days after activation**. 

Schedule configuration is coming soon.. check for updates

-----------
Versioning
-----------

I use `SemVer <http://semver.org/>`_ for versioning. For the versions available, see the `tags on this repository <https://github.com/tmxak/aws-datapipe/tags>`_. 

-------
Author
-------

* **Maxim Tacu** - Site Reliability Engineer - `OLX Group <https://www.olxgroup.com/>`_.

-------
License
-------

This project is licensed under the MIT License - see the `LICENSE <LICENSE>`_ file for details


How to Contribute
-----------------

Contributions are very welcome. The easiest way is to fork this repo, and then
make a pull request from your fork.