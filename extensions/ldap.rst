.. include:: ../GLOBAL.rst

.. _ldap_auth:

Enable LDAP Authentication
===========================

When LDAP is activated, it will move the authentication and user management outside of |SCALR| and hand it over to the LDAP server that you have configured. Each |ACCOUNT| in Scalr can have a separate LDAP provider if your organization requires it.

Configuration
^^^^^^^^^^^^^
To enable LDAP, you must configure it in the global area of the |SCALR| UI. To do this:

1. Log in as a global admin, click on the |SCALR| icon on the top left and go to IAM -> identity providers:

        .. image:: /images/ldap_setup.png
           :width: 500

2. Fill in the fields required by your LDAP server.

3. After you save the LDAP configuration, link the provider to an |ACCOUNT|:

        .. image:: /images/ldap_account.png
           :width: 500

Users and Teams with LDAP
^^^^^^^^^^^^^^^^^^^^^^^^^

After Scalr has been reconfigured for LDAP, users and teams work as follows.

1. Teams map to AD/LDAP groups. Account admins still have to create teams in |SCALR| but the team name will be validated against the groups in AD/LDAP, so the team name must match the group name.
2. Teams must linked to at least one |ENVIRONMENT|
3. Once a team has been linked, any member of the related LDAP group can attempt to login to |SCALR|. On first login a user record gets created in |SCALR| and set as LDAP authenticated.
4. |SCALR| admin can still create |SCALR| authenticated users to act as global and |ACCOUNT| admins. SAML authenticated users can also be set as global and |ACCOUNT| admins.
5. If a user has access to more than one account, they will be prompted to select an account during login.

.. note:: |SCALR_SERVER_RB|
