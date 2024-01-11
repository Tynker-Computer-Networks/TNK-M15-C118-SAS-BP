Send the Email
===========================


In this activity, you will learn to add the functionality to send the email when the "Send Email" button is clicked.


<img src= "https://s3.amazonaws.com/media-p.slid.es/uploads/1525749/images/10905315/pasted-from-clipboard.png" width = "480" height = "320">




Follow the given steps to complete this activity:


1. Fetch the credentials and the message.
* Get the values from the widgets.
~~~sh
        sender_email = self.sender_email_entry.get()
        sender_password = self.sender_password_entry.get()
        recipient_email = self.recipient_email_entry.get()
        subject = self.subject_entry.get()
        message_body = self.message_body_text.get("1.0", "end")
~~~


2. Send the email when the button is clicked. 
* Place the order by uncommenting the `placeOrder` function definition.
~~~sh
self.send_button = Button(
            self.frame, text="Send Email", command=self.send_single_email)
~~~
* Save and run the code to check the output.
