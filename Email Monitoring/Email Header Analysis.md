Email Internet Header - A record of the email servers involved in transferring an email message from a sender to a recipient

Attackers exploit the fact that there are actually three sender address fields in an email
1. Display From - Typically what you see as the sender in an email GUI client
2. Envelope From - Various labels hidden from mail client (return address)
3. Received From/By - List of MTAs that processed email

Most headers are not displayed by email applications by default

X-headers indicate custom headers that are controlled by the SMTP server administrator

