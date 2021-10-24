.. include:: ../GLOBAL.rst

Enable SAML Authentication
===========================

Integration with Scalr
^^^^^^^^^^^^^^^^^^^^^^
When SAML is activated, it will move the authentication step outside of Scalr and hand it over to the SAML server that you have configured. During sign in to Scalr, the user will be transferred to a sign in page provided by the SAML server. After sign in, the user will then be redirected back to Scalr which will subsequently treat the user as signed in.

Configuration
^^^^^^^^^^^^^
To enable SAML, you must configure it in the global area of the Scalr UI. To do this:

1. Log in as a global admin, click on the Scalr icon on the top left and go to IAM -> identity providers:

        .. image:: /images/saml_setup.png
           :width: 500

2. Note down the SP endpoint as that will be used with the SAML provider. For example: ``https://scalr.server/public/saml/idp-sp986542njcvhjv78?metadata`` and ``https://scalr.server/public/saml/idp-sp986542njcvhjv78?acs``

3. Fill in the fields required by your SAML provider.

4. After you save the SAML configuration, link the provider to an |ACCOUNT|:

        .. image:: /images/saml_account.png
           :width: 500

.. note:: In the event you need to log in with a local administrator, add the following to the end of your Scalr url to avoid the SAML login screen: ``#?no-login-redirect`` (``https://your.scalrserver.com#?no-login-redirect``)

.. note:: |SCALR_SERVER_RB|
