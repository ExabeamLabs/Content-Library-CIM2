#### Parser Content
```Java
{
Name = symantec-esc-json-email-send-success-emailinfo
   ParserVersion = v1.0.0
   Vendor = Symantec
   Product = Email Security.cloud
   TimeFormat = "epoch_sec"
   Conditions = [
"""emailInfo""",
"""HELOString""",
""""isOutbound":true"""
   ]
   Fields = [
     """"mailProcessingStartTime"+:({time}\d{10})""",
     """"headerFrom":"({email_address}[^"]+)",""",
     """"subject":"({email_subject}[^"]+)",""",
     """"messageSize":({bytes}\d+)""",
     """"messageId":"({alert_id}[^"]+)",""",
     """"headerTo":\[({email_recipients}[^\]]+)\],""",
     """"headerTo":\["({dest_email_address}[^"@]+@[^@"]+)"""",
     """"isOutbound":({direction}[^,]+),""",
     """"senderIp":"({src_ip}[a-fA-F\d.:]+)""",
     """\[\{"fileNameOrURL":"({email_attachment}[^\.]+\.({file_ext}[^"]+))"""
   ]
 

}
```