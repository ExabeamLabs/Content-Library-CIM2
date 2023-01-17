#### Parser Content
```Java
{
Name = symantec-esc-json-email-send-success-emailinfo
   ParserVersion = v1.0.0
   Vendor = Symantec
   Product = Symantec Email Security
   TimeFormat = "epoch_sec"
   Conditions = [
"""emailInfo""",
"""HELOString""",
""""isOutbound":true"""
   ]
   Fields = [
     """"mailProcessingStartTime"+:({time}\d{10})""",
     """"headerFrom":"({sender}[^"]+)",""",
     """"subject":"({email_subject}[^"]+)",""",
     """"messageSize":({bytes}\d+)""",
     """"messageId":"({alert_id}[^"]+)",""",
     """"headerTo":\[({email_recipients}[^\]]+)\],""",
     """"headerTo":\["({dest_email_address}[^"@]+@[^@"]+)"""",
     """"isOutbound":({direction}[^,]+),""",
     """"senderIp":"({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
     """\[\{"fileNameOrURL":"({email_attachment}[^\.]+\.({file_ext}[^"]+))"""
   ]
  DupFields = [ "sender->email_user" , "dest_email_address->external_address" , "email_attachment->file_name"]
 

}
```