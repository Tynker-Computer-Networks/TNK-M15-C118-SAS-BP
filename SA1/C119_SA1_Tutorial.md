Display Email Details
===================


In this activity, you will activate the 2-step google authentication on google accounts and create a secure password for email.




<img src= "https://s3.amazonaws.com/media-p.slid.es/uploads/1525749/images/10899396/118_oucome.gif" width = "180" height = "320">


Follow the given steps to complete this activity:
1. Activate 2-Step Authentication.


* Open file app.py


* Activate the 2-step authentication.


* Get the app password.


* Create an instance for email sending.
	```
class EmailSenderApp():
    		def __init__(self):
        		super().__init__()
	```
* Accept email details and print it.
```
def send_single_email(self):
sender_email = input("Enter Sender Email\n")
        	sender_password = input("Enter Sender Password\n")


  	print("Sender Email: ",sender_email)
        	print("Sender Password: ",sender_password)
	```
   
* Display the email details by creating a class object and calling the ‘send_single_email()’ and ‘main()’ function.
 	```
     	def main():
            app = EmailSenderApp()
            app.send_single_email()


if __name__ == "__main__":
        	main()’
      
``` 
* Save and run the code to check the output.
