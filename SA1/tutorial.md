Create the GUI
============================


In this activity, you will learn to create the widgets and place them using the grid geometric manager.


<img src= "https://s3.amazonaws.com/media-p.slid.es/uploads/1525749/images/10899351/pasted-from-clipboard.png" width = "480" height = "320">


Follow the given steps to complete this activity:


1. Create the frame.


* Open the `main.py` file.


* Create a frame and place it on the window.
~~~sh
class EmailSenderApp(Tk):
    def __init__(self):
        super().__init__()
        self.title("Email Sender")
        self.frame = Frame()
        self.frame.grid(column=0,row=0,padx=10,pady=10)
~~~
2. Create the widget and place them on the frame.
* Create the widgets for the inputs required in an email and place the widgets on the frame by using the grid.
~~~sh
Label(self.frame, text="Sender's Email:").grid(
            column=0, row=0, sticky="w")
        self.sender_email_entry = Entry(self.frame)
        self.sender_email_entry.grid(
            column=1, row=0, padx=10, pady=5, columnspan=2)


        Label(self.frame, text="Sender's Password:").grid(
            column=0, row=1, sticky="w")
        self.sender_password_entry = Entry(self.frame, show="*")
        self.sender_password_entry.grid(
            column=1, row=1, padx=10, pady=5, columnspan=2)


        Label(self.frame, text="Recipient's Email:").grid(
            column=0, row=2, sticky="w")
        self.recipient_email_entry = Entry(self.frame)
        self.recipient_email_entry.grid(
            column=1, row=2, padx=10, pady=5, columnspan=2)


        Label(self.frame, text="Subject:").grid(column=0, row=3, sticky="w")
        self.subject_entry = Entry(self.frame)
        self.subject_entry.grid(column=1, row=3, padx=10, pady=5, columnspan=2)
        Label(self.frame, text="Message:").grid(column=0, row=4, sticky="w")
        self.message_body_text = Text(self.frame, width=40, height=10)
        self.message_body_text.grid(
            column=1, row=4, padx=10, pady=5, columnspan=2)
        self.send_button = Button(self.frame, text="Send Email")
        self.send_button.grid(column=1, row=9, padx=10, pady=10, columnspan=2)
~~~


* Save and run the code to check the output.
