#### Parser Content
```Java
{
Name = symantec-esc-json-email-send-success-fileincluded
ExtractionType = json
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
  """"envFrom":\s*"({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))"""
  """"envTo":\s*\[({email_recipients}"({dest_email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({dest_email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))".*?)\]"""
  """"subject":\s*"\s*({email_subject}.+?)\s*""""
  """"senderIp":\s*"*({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
  """"fileNameOrURL":\s*"({email_attachment}[^"]+)"""
  """"severity":\s*"({alert_severity}[^"]+)"""
  """"securityService":\s*"({alert_type}[^"]+)""""
  """"action":\s*"({action}[^"]+)"""
  """"malwareName":\s*"(null|unknown|({alert_name}[^"]+))"""
  """"malwareCategory":\s*"({threat_category}[^"]+)"""
  """"messageSize":\s*({bytes}\d+)"""
  """exa_json_path=$.emailInfo.mailProcessingStartTime,exa_field_name=time"""
  """exa_json_path=$.emailInfo.isOutbound,exa_field_name=is_outbound"""
  """exa_json_path=$.emailInfo.envFrom,exa_regex=({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))"""
  """exa_regex="envTo":\s*\[({email_recipients}"({dest_email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({dest_email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))".*?)\]"""
  """exa_json_path=$.emailInfo.subject,exa_field_name=email_subject"""
  """exa_json_path=$.emailInfo.senderIp,exa_field_name=src_ip"""
  """exa_regex="fileNameOrURL":\s*"({email_attachment}[^"]+)"""
  """exa_regex="severity":\s*"({alert_severity}[^"]+)"""
  """exa_regex="securityService":\s*"({alert_type}[^"]+)""""
  """exa_regex="action":\s*"({action}[^"]+)"""
  """exa_regex="malwareName":\s*"(null|unknown|({alert_name}[^"]+))"""
  """exa_regex="malwareCategory":\s*"({threat_category}[^"]+)"""
  """exa_regex="messageSize":\s*({bytes}\d+)"""]
ParserVersion = "v1.0.0"


}
```