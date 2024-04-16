#### Parser Content
```Java
{
Name = trendmicro-scanmail-json-alert-trigger-success-wineventlog
ExtractionType = json
Vendor = "Trend Micro"
Product = "Trend Micro ScanMail"
TimeFormat = "MM/dd/yyyy HH:mm:ss a"
Conditions = [
  """has been detected"""
  """has been taken on"""
  """Message details:"""
]
Fields = [
  """exa_regex=(|({alert_name}[^"]+?))\s+has been detected,and\s+(|({result}.+?))\s+has been taken on\s+({time}\d+\/\d+\/\d+\s+\d+:\d+:\d+\s+(PM|AM|pm|am)).\\nMessage details:\\nServer:\s*(|({host}[\w.\-]+))\\nFound in:\s*(|({alert_type}.+?))\\nSender:\s*(|({malware_url}.+?));\\nRecipient:\s*(|({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+)));\\nSubject:\s*(|({additional_info}.+?))\s*\\nAttachment name:\s*(|({file_name}[^"]+?))("|\s*$)"""
  """exa_json_path=$.host.name,exa_field_name=src_host"""
  """exa_json_path=$.level,exa_field_name=alert_severity"""
]
ParserVersion = "v1.0.0"


}
```