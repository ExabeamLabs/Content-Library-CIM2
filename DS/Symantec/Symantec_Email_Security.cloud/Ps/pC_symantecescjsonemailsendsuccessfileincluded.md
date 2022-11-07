#### Parser Content
```Java
{
Name = symantec-esc-json-email-send-success-fileincluded
Vendor = "Symantec"
Product = "Symantec Email Security.cloud"
TimeFormat = "epoch_sec"
Conditions = [
  """"mailProcessingStartTime": """
  """"isOutbound": """
  """"envFrom": """
  """"senderIp": """
]
Fields = [
  """"mailProcessingStartTime":\s*({time}\d+)"""
  """"isOutbound":\s*({is_outbound}[^,]+)"""
  """"envFrom":\s*"({email_address}[^"@]+@[^"@]+)"""
  """"envTo":\s*\[({email_recipients}"({dest_email_address}[^"@]+@[^"@]+)".*?)\]"""
  """"subject":\s*"\s*({email_subject}.+?)\s*""""
  """"senderIp":\s*"*({src_ip}[a-fA-F\d.:]+)"""
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