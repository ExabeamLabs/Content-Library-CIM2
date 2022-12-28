#### Parser Content
```Java
{
Name = symantec-esc-json-email-receive-success-emailinfo
   ParserVersion = v1.0.0
   Vendor = Symantec
   Product = Symantec Email Security
   TimeFormat = "epoch_sec"
   Conditions = [
"""emailInfo""",
"""HELOString""",
""""isOutbound":false"""
   ]
   Fields = [
     """"mailProcessingStartTime"+:({time}\d{10})""",
     """"headerFrom":"({email_address}[^"@]+@[^@"]+)",""",
     """"subject":"({email_subject}[^"]+)",""",
     """"messageSize":({bytes}\d+)""",
     """"messageId":"({alert_id}[^"]+)",""",
     """"headerTo":\[({email_recipients}[^\]]+)\],""",
     """"headerTo":\["({dest_email_address}[^"]+)"""",
     """"isOutbound":({direction}[^,]+),""",
     """"senderIp":"({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
   ]
 

}
```