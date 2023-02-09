#### Parser Content
```Java
{
Name = trendmicro-scanmail-json-alert-trigger-success-wineventlog
Vendor = "Trend Micro"
Product = "Trend Micro ScanMail"
TimeFormat = "MM/dd/yyyy HH:mm:ss a"
Conditions = [
  """has been detected"""
  """has been taken on"""
  """Message details:"""
]
Fields = [
  """(|({alert_name}[^"]+?))\s+has been detected,and\s+(|({action}.+?))\s+has been taken on\s+({time}\d+\/\d+\/\d+\s+\d+:\d+:\d+\s+(PM|AM|pm|am)).\\nMessage details:\\nServer:\s*(|({host}[\w.\-]+))\\nFound in:\s*(|({alert_type}.+?))\\nSender:\s*(|({malware_url}.+?));\\nRecipient:\s*(|({email_address}.+?));\\nSubject:\s*(|({additional_info}.+?))\s*\\nAttachment name:\s*(|({file_name}[^"]+?))("|\s*$)"""
  """"hostname":"({src_host}[^"]+)"""
  """"level":"({alert_severity}[^"]+)"""
]
ParserVersion = "v1.0.0"


}
```