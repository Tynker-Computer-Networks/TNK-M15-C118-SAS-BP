Display the Message Box
===================




In this activity, you will learn display the information in the message box.




<img src= "https://s3.amazonaws.com/media-p.slid.es/uploads/1525749/images/10908256/pasted-from-clipboard.png" width = "480" height = "320">


Follow the given steps to display the error and success messages in a message box:


1. Display the Message.
* Open the files `main.py`.
* Display the message after the email is sent by displaying the message box with the information.
~~~python
from tkinter import messagebox
. . .
def send_single_email(self):
  try:
           ...
       	messagebox.showinfo("Email Sent", "Email sent successfully!")
           ...
  except Exception as e:
            messagebox.showerror("Error", f"An error occurred: {str(e)}")
~~~


2. Send Multiple Emails.


* Send multiple emails using multithreading.
~~~python
def send_email(self):
        threading.Thread(target=self.send_single_email).start()

self.send_button = Button(
            self.frame, text="Send Email", command=self.send_email)
~~~
* Save and run the code to check the output.
