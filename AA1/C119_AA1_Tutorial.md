Send Email to Multiple Addresses
=================




In this activity, you will learn to send the email to multiple recipients.


<img src= "https://media.slid.es/uploads/1525749/images/10932908/AA1.gif" width = "480" height = "320">


Follow the given steps to complete this activity:
	
1. Create and Place the Reqired Widgets.


* Open the file `main.py`.


* Create a button widget to add new recipients.
~~~python
        self.add_button = Button(self.frame, text="Add Recipient", command=self.add_recipient)
        self.add_button.grid(column=1, row=3, padx=10, pady=5, columnspan=2)


~~~
* Create a listbox to display the recipients.
~~~python
        Label(self.frame, text="Recipients List:").grid(column=0, row=4, sticky="w")
        self.recipients_listbox = Listbox(self.frame)
        self.recipients_listbox.grid(column=1, row=4, padx=10, pady=5, columnspan=2)


~~~


2. Add and Display the Recipients.
* Create a list and add the recipients to the list.
~~~python
class EmailSenderApp(Tk):
    def __init__(self):
	  . . .
        self.recipients_email = []


    def add_recipient(self):
        email = self.recipient_email_entry.get()
        if(email):
            self.recipients_email.append(email)
            self.update_listbox()
            self.recipient_email_entry.delete(0, END)
    def update_listbox(self):
        self.recipients_listbox.delete(0, END)
        for recipient in self.recipients_email:
            self.recipients_listbox.insert(END, recipient)
~~~
3. Send the email to all the recipients.
* Use loop to send the email to each recipient.
~~~python
for recipient_email in self.recipients_email:
            try:
                . . .
            except Exception as e:
                . . .


~~~


* Save and run the code to check the output.
