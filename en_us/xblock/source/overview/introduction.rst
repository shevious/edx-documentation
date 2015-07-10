.. _Introduction to XBlocks:

#############################
Introduction to XBlocks
#############################

.. include:: ../reusable/introduction_text.rst

.. contents::
 :local:
 :depth: 1

*****************************
XBlock API and Runtimes
*****************************

XBlock is an API than can be used by different applications, referred to as
XBlock :ref:`runtimes<XBlock Runtimes>`.

As described below, the edX Platform uses the XBlock API, and is the most
common XBlock runtime.

 If you are planning to use your XBlock in a different rutime, check the
 documentation to understand the runtime's requirements.

*****************************
XBlocks and the edX Platform
*****************************

The edX Platform uses many built-in XBlocks that are available to course
developers. For example, HTML content, videos, and interactive problems are all
XBlocks. The edX Platform also includes many specialized XBlocks such as
`Google Drive`_ and `Open Response Assessments`_. For more information, see
:ref:`XBlocks and the edX Platform`.

EdX recognizes the ever expanding need to provide new and innovative types
of content. The XBlock API and XBlock SDK are available for developers to
create new types of XBlocks for course teams to use.

***********************
XBlocks for Developers
***********************

Developers can extend the types of content available in the edX Platform by
creating and deploying XBlocks. EdX provides the `XBlock SDK`_ to support the
creation of new XBlocks.

===================
Prerequisites
===================

This tutorial is for developers who are new to XBlock. To use this tutorial,
you should have basic knowledge of the following technologies.

* Python
* JavaScript
* HTML and CSS
* Python virtualenv
* Git

===================
XBlock Resources
===================

This tutorial is meant to guide developers through the process of creating an
XBlock, and to explain the :ref:`concepts<XBlock Concepts>` and
:ref:`anatomy<Anatomy of an XBlock>` of XBlocks.

Developers should also see the XBlock API documentation. [ADD LINK]

=========================================
XBlock Independence and Interoperability
=========================================

You must design your XBlock to meet two goals.

* The XBlock must be independent of other XBlocks. Course teams must be able to
  use the XBlock without using other XBlocks.

* The XBlock must work together with other XBlocks. Course teams must be
  able to combine different XBlocks in flexible ways.

=========================================
XBlocks Compared to Web Applications
=========================================

XBlocks are similar to web applications. XBlocks maintain state in a storage
layer, render themselves through views, and process user actions through
handlers.

XBlocks differ from web applications in that they render only a small piece of
a complete web page.

.. include:: ../links.rst