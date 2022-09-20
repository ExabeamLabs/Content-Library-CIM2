#### Parser Content
```Java
{
Name = rsa-dlp-kv-alert-trigger-success-glba
  Vendor = RSA
  Product = RSA DLP
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Conditions = [ """DLP_EM:""", """usage=""", """usageApplication=""" ]
  Fields = [
    """DLP_EM:\s*({host}[^\s]+)""",
    """User=(({domain}[^\\]+)\\)?({user}.+?)\s+\w+=""",
    """Incident\s*:*\s*"({alert_name}[^"]+)""",
    """Severity=({alert_severity}[^\s]+)""",
    """Policy=({alert_type}.+?)\s+\w+=""",
    """userEmail=({email_address}[^\s]+)""",
    """action=({action}.+?)\s+\w+=""",
    """usage=({alert_type}.+?)\s+\w+=""",
    """usageIp=({src_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})""",
    """usageApplication=({process_path}({process_dir}(?:(\w+:)?[^:]+)?[\\\/])?({process_name}.+?))\s+\w+="""
  ]
  ParserVersion = "v1.0.0"


}
```