#### Parser Content
```Java
{
Name = symantec-esc-json-email-send-success-fileincluded
Vendor = "Symantec"
Product = "Symantec Email Security"
TimeFormat = "epoch_sec"
Conditions = [
  """"mailProcessingStartTime": """
  """"isOutbound": """
  """"envFrom": """
  """"senderIp": """
]
Fields = [
  """"mailProcessingStartTime":\s*({time}\d{10})"""
  """"isOutbound":\s*({is_outbound}[^,]+)"""
  """"envFrom":\s*"({src_email_address}[^"@]+@[^"@]+)"""
  """"envTo":\s*\[({email_recipients}"({dest_email_address}[^"@]+@[^"@]+)".*?)\]"""
  """"subject":\s*"\s*({email_subject}.+?)\s*""""
  """"senderIp":\s*"*({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
  """"fileNameOrURL":\s*"({email_attachment}[^"]+)"""
  """"severity":\s*"({alert_severity}[^"]+)"""
  """"securityService":\s*"({alert_type}[^"]+)""""
  """"action":\s*"({action}[^"]+)"""
  """"malwareName":\s*"(null|unknown|({alert_name}[^"]+))"""
  """"malwareCategory":\s*"({threat_category}[^"]+)"""
  """"messageSize":\s*({bytes}\d+)"""
]
ParserVersion = "v1.0.0"


}
```