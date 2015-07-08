.. _Set Up the XBlock Software Development Kit:

###########################################
Set Up the XBlock Software Development Kit
###########################################

Before you continue, make sure that you are familiar with the subjects in the 
:ref:`Install XBlock Prerequisites` section.

When you have installed all prerequisites, you are ready to set up the `XBlock
SDK`_ in a virtual environment. To do this, complete the following steps.

.. contents::
 :local:
 :depth: 1

********************************************
Create a Directory for XBlock Work
********************************************

It is recommended that you create a directory in which to store all your XBlock
work, including a virtual environment, the XBlock SDK, and the XBlocks you
develop.

At the command prompt, run the following command to create the directory.
   
   .. code-block:: bash

      $ mkdir my_xblock_development

.. _Create and Activate the Virtual Environment:

********************************************
Create and Activate the Virtual Environment
********************************************

The first step is to create the virtual environment in your
``my_xblock_development`` directory.

#. At the command prompt in ``my_xblock_development``, run the following
   command to create the virtual environment.
   
   .. code-block:: bash

      my_xblock_development $ virtualenv venv

#. Run the following command to activate the virtual environment.

   .. code-block:: bash
  
      $ source venv/bin/activate

   When the virtual environment is activated, the command prompt shows the name
   of the virtual directory in parentheses.

   .. code-block:: bash
     
      (venv)xblock my_username $

.. include:: ../reusable/clone_sdk.rst

When the requirements are installed, you are ready to create your first XBlock.

.. include:: ../links.rst
