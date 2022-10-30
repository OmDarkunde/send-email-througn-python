# send-email-througn-python

import smtplib , ssl # smtp - Simple Mail Transfer Protocol. , ssl - secure sockets layer
port = 465  # For SSL
smtp_server = "smtp.gmail.com"
sender_email = "omdarkunde4@gmail.com"  # Enter your address
receiver_email = "sudhanshu@ineuron.ai"  # Enter receiver address
password = 'pwjmiddjcemntwor'
message = """this is my message from python code in my live class """

context = ssl.create_default_context()
with smtplib.SMTP_SSL(smtp_server, port, context=context) as server:
    server.login(sender_email, password)
    server.sendmail(sender_email, receiver_email, message) 
