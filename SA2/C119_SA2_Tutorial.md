Setup SMTP Server
===================


In this activity, you will set up the SMTP server and store the email details in the server template.






<img src= "https://s3.amazonaws.com/media-p.slid.es/uploads/1525749/images/10899397/118_2nd_otcome.gif" width = "50%" height = "auto">




Follow the given steps to complete this activity:
1. Setup SMTP Server.


* Open the file app.py.


* Import ‘smtplib’, ‘MIMEText’, ‘MIMEMultipart’ Libraries.
	
	```
import smtplib
from email.mime.text import MIMEText
from email.mime.multipart import MIMEMultipart
```


* Setup the SMTP server, secure information and login.
	```
smtp_server = smtplib.SMTP("smtp.gmail.com", 587)
      smtp_server.starttls()
      smtp_server.login(sender_email, sender_password)
	```


* Create and send the email template.
```
message = MIMEMultipart()
      message["From"] = sender_email
      message["To"] = recipient_email
      message["Subject"] = subject    
      message.attach(MIMEText(message_body, "plain"))
```


* Save and run the code to check the output.
