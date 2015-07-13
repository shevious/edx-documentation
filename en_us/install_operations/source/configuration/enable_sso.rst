
.. _Enabling Third Party Authentication:

#################################################################
Enabling Third Party Authentication for Single Sign On (SSO)
#################################################################

You enable third party authentication for your implementation of the edX
platform to enhance sign in capabilities for your users. After you enable third
party authentication, users can register and sign in with their campus or
institutional credentials to access courses.

.. contents::
   :local:
   :depth: 1

*****************************************************************
Obtain a Client ID and Secret from the OAuth2 Provider
*****************************************************************

In order to add a new OAuth2 provider to your edX installation, you will first have to go to the provider's site to register your edX installation with that provider and obtain a client ID and secret for your installation. All OAuth2 providers have well defined interfaces for doing this.

************************************
Enable Third Party Authentication
************************************

By default, third party authentication is not enabled on edX installations. To enable it, follow these steps.

#. In the ``edx/app/edxapp/lms.env.json`` file, edit the file so that it
   includes the following line in the features section.

   .. code-block:: json

       "FEATURES" : {
           ...
           "ENABLE_THIRD_PARTY_AUTH": true
       }

#. Save the ``edx/app/edxapp/lms.env.json`` file.

.. does "ENABLE_COMBINED_LOGIN_REGISTRATION": true also need to be set? 

*****************************************************************
Add the Provider to your Configuration
*****************************************************************

For security reasons, every installation needs to maintain a list of approved OAuth2 providers called a whitelist. To add a new provider to the whitelist, follow these steps.

#. Ensure that the python-social-auth backend class for the provider that you
   want to use is accessible by your edX installation. For example, verify that
   the Django ``AUTHENTICATION_BACKENDS`` setting for the LMS contains
   ``third_party_auth.saml.SAMLAuthBackend``.

   If you are using the ``aws`` environment or a derived environment such as
   devstack, the ``lms/envs/aws.py`` script sets this class for you.

#. To customize the list of providers, edit the ``lms.env.json`` file to add
   the backend class to ``"THIRD_PARTY_AUTH_BACKENDS"``.

=================================================================
Add or Configure an Approved Provider
=================================================================

To enable and configure an OAuth2 client that is on the whitelist, follow these steps.

#. Log in to the Django administration console for your base URL. For example,
   ``http://{your_URL}/admin``.

#. In the **Third_Party_Auth** section, next to **Provider Configuration
   (OAuth2)** select **Add**.

   To change the configuration of a provider, next to **Provider Configuration
   (OAuth2)** select **Change**, and then select the provider that you want to
   configure.

#. On the Add Provider Configuration page, enter the following required
   information.

 - **Icon class**: The icon class for the button that you want to include on
   the sign in page.
 - **Name**: The name of the authentication provider, as it you want it to
   appear on the sign in page.
 - **Backend name**: Select a python-social-auth backend class from your
   whitelist.
 - **Client ID**
 - **Client Secret**

#. Specify your selections for other configuration options. For more
   information about these options, see :ref:`Configuration Options for OAuth2
   Providers`.

#. When you are ready to enable the provider, select **Enabled** You can save
   your configuration settings and enable the provider at another time.

#. Select **Save**.

#. To verify that users can use a provider that you have enabled, go to the
   sign in page for your LMS. The page should include a button with the
   selected icon class. If the class is ``fa-sign-in``,

.. _Configuration Options for OAuth2 Providers:

=================================================================
Configuration Options for OAuth2 Providers
=================================================================


Provider Prominence
**************************

The list of providers enabled for an edX installation can be divided into two categories: Primary and Secondary. Providers from the primary list are displayed prominently on the login / registration pages (with a button). Secondary providers are displayed less prominently, in a separate list of "Institution" login providers.

Here is an example of the signin page for primary providers:

.. image:: ../Images/signin.png
 :alt: Image showing the edX primary signin page

Here is an example of the signin page for secondary providers: 

.. image:: ../Images/secondary_signin.png
 :alt: Image showing the edX secondary signin page

You can specify whether a provider is Primary or Secondary via the Third Party Auth -> Provider Configuration (OAuth2) admin page.


Streamline Registration
**************************

In order to make the registration process simpler, edX makes it possible to simply absorb the user's details (such as name, email etc.) silently from their OAuth2 provider instead of asking them to confirm them. This option should be used only for trusted providers that are known to provide accurate user information.

You can specify whether to skip the registration form on a per-provider basis via the Third Party Auth -> Provider Configuration (OAuth2) page.


Activation Email Message
**************************

At the end of the registration process, edX sends an email to the email address provided during registration to confirm the identity of the user. For trusted providers, the admin can choose to skip this part so users will not be required to confirm their email, and their account will be activated immediately upon registration.

You can specify whether to skip the email verification step during the registation process via the Third Party Auth -> Provider Configuration (OAuth2) page.

======================================================================
Specify default third party authentication via QueryString parameter
======================================================================

If the link to a course includes a query parameter (tpa_hint) that specifies one of the enabled third party authentication providers, and the user is not logged in to that provider, the third party authentication sign in flow with the specified provider will be automatically started instead of redirecting the user to the login page.
