Send a CC of the Email
==============




In this activity, you will learn to send a CC of the email to the specified recipient.




<img src= "https://media.slid.es/uploads/1525749/images/10932913/pasted-from-clipboard.png" width = "350" height = "450">


Follow the given steps to complete this activity:
1. Create the Required Widgets.
* Open the file `main.py`.
* Create a label and a textbox to enter the address.
~~~python
        Label(self.frame, text="CC:").grid(column=0, row=5, sticky="w")
        self.cc_entry = Entry(self.frame)
        self.cc_entry.grid(column=1, row=5, padx=10, pady=5, columnspan=2)
~~~
2. Send the CC of the email to the recipient.
~~~python
def send_single_email(self):
        . . . 


        for recipient_email in self.recipients_email:
            try:
                . . .
                message["Cc"] = self.cc_entry.get()


~~~
* Save and run the code to check the output.
