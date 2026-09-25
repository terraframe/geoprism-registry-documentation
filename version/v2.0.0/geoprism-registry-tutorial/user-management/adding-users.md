# Adding users

{% hint style="info" %}
System Administrators and Registry Administrators can be added to the system by a System Administrator. Registry Maintainers and Registry Contributors for an organization can be added by a Registry Administrator for the organization the users are being added to.
{% endhint %}

To let someone set up their own account instead, [invite them](inviting-users.md).

1.  Go to the **Settings** page from the sidebar.

    ![](<../../../../.gitbook/assets/image (28).png>)
2.  In the **User Accounts** section, click **Manage Accounts**.

    <figure><img src="https://lh5.googleusercontent.com/iY-i15Toiw8x_IO2Tmxo--MzNbW32pqAzGdaIDnYq2HF9DkMbpW0aCEqJlH-POq8K0if0rCmUdNqNVzGHTtOD5Vc5iXXlYMrZsqbqWJ4Kjk9Bp3Mxpd_mpqa3sCP1VOc8e9SiNZ-FpTICUlucI6syM3amu29aioueQ822aQz_C8Zmqn_dXQEktMy" alt=""><figcaption></figcaption></figure>
3.  The list of existing users opens. Click the plus icon (**Add new user**) at the bottom of the list.

    <figure><img src="https://lh5.googleusercontent.com/YESK1fozcAcYrPuZBbKlmK5SgFLb-0ctB2a7f_QQUWwiP9v0P7Ia2ckAoC-TcLyfpx_0zv0g1VlYjRH8lj_hOQGm0Sz6GWy8UuSofxOO3uQ3lUCS9hJoUNIvsBAHOJ3J4d7HCoYdQGPLO7ctR_sUopC1owKBQMy2kJgJT_CEss6dMs3-8RdCAf0n" alt=""><figcaption></figcaption></figure>
4.  Fill out the **Account** form:

    | Field | Description | Required |
    | ----- | ----------- | -------- |
    | First name, Last name | The user's name. | Required |
    | First name (local), Last name (local) | The user's name in another language. | |
    | Phone Number, Phone number 2 | The user's phone numbers. | |
    | Email Address | The user's email address. Password reset emails are sent here. | Required |
    | Position/Function | The user's position or function in their organization. | |
    | Department | The department the user belongs to. | |
    | Username | The name the user logs in with. It's also shown wherever the app identifies the user. | Required |
    | OAuth | Only shown if an external system with OAuth is registered. Click **Enable OAuth** and choose the **External System** to let the user log in through that system instead of with a password. | |
    | New password, Confirm new password | The user's password. The two fields must match. | Required |
    | User Status | **Active** (the default) lets the user log in and use their roles. **Inactive** prevents the user from using the system without deleting the account. | |
    | Roles | <p>What the user can do. At least one role is required.</p><ul><li><strong>System Administrator:</strong> full access to the whole system. Only a System Administrator can assign it.</li><li><strong>Registry Administrator</strong> for an organization. Only a System Administrator can assign it.</li><li>For each Geo-Object Type in an organization, a role such as <strong>Registry Maintainer</strong> or <strong>Registry Contributor</strong>, or <strong>None</strong>.</li></ul><p>A user can only have roles in one organization. See <a href="../../geoprism-registry-key-components/user-roles-and-rights/README.md">User roles and rights</a>.</p> | Required |
5.  Click **Submit**.
