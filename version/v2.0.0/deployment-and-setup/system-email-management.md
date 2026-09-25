# System email management

Geoprism Registry sends emails to users, such as account invitations, password resets and change request notifications. It can't send email by itself: it connects to an email server that sends the messages for it. Only a System Administrator can configure email.

{% hint style="info" %}
Geoprism Registry only works with SMTP (Simple Mail Transfer Protocol) email servers.
{% endhint %}

1.  Go to the **Settings** page from the sidebar.

    ![](<../../../.gitbook/assets/image (28).png>)
2.  In the **Email** section, click **Configure**.

    <figure><img src="https://lh5.googleusercontent.com/ZOkJTcRXypi14doj0e9FN3ni6gwQxORSUwloulUcNibVGl3q7sk7SnzuxLEGgEn4siJeBEElaKYIsiLsnpgW2SefSANWdCRDXwQhiKJSRPA99YhcbHFipPfqzRPe2ACq-BPhEJBM6KF_b2N9lN1SjGM-YcHp2sYeo1LfELkAhCvlPu40frJb6XnS" alt=""><figcaption></figcaption></figure>
3.  Fill out the **Email Server** form:

    | Field | Description | Required |
    | ----- | ----------- | -------- |
    | Server | The address of the SMTP server, for example `email-smtp.us-west-2.amazonaws.com`. | Required |
    | User name | A user that can send email through the server. | Required |
    | Password | That user's password. | Required |
    | Port | The port the SMTP server accepts connections on. It's set on the email server, not on Geoprism Registry. | Required |
    | From | The email address that emails are sent from. | Required |
    | To | An email address that receives emails from the system. | |
4.  Click **Submit**. The **Email** section shows **Configured** once email is set up.
