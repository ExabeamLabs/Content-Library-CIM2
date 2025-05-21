#### Parser Content
```Java
{
Name = symantec-esc-json-email-receive-success-emailinfo
   ParserVersion = v1.0.0
   Vendor = Symantec
   Product = Symantec Email Security
   TimeFormat = "epoch_sec"
   ExtractionType = json
   Conditions = [ """emailInfo""", """HELOString""", """"isOutbound":false""" ]
   Fields = [
     """"mailProcessingStartTime"+:({time}\d{10})""",
     """"headerFrom":"({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))",""",
     """"subject":"({email_subject}[^"]+)",""",
     """"messageSize":({bytes}\d+)""",
     """"messageId":"({alert_id}[^"]+)",""",
     """"headerTo":\[({email_recipients}[^\]]+)\],""",
     """"headerTo":\["({dest_email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({dest_email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))"""",
     """"isOutbound":({direction}[^,]+),""",
     """"senderIp":"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""

     """exa_json_path=$.emailInfo.mailProcessingStartTime,exa_field_name=time""",
     """exa_json_path=$.emailInfo.headerFrom,exa_regex=^({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))$""",
     """exa_json_path=$.emailInfo.subject,exa_field_name=email_subject""",
     """exa_json_path=$.emailInfo.messageSize,exa_field_name=bytes""",
     """exa_json_path=$.emailInfo.messageId,exa_field_name=alert_id""",
     """exa_json_path=$.emailInfo.headerTo[0],exa_field_name=email_recipients""",
     """exa_json_path=$.emailInfo.headerTo[0],exa_regex=^({dest_email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({dest_email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))$""",
     """exa_json_path=$.emailInfo.isOutbound,exa_field_name=direction""",
     """exa_json_path=$.emailInfo.senderIp,exa_regex=^({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?$"""
   ]
 

}
```