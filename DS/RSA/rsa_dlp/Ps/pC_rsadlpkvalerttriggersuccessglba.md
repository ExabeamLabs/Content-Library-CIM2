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
    """User=(({domain}[^\\]+)\\)?({user}[\w\.\-\!\#\^\~]{1,40}\$?)\s+\w+=""",
    """Incident\s*:*\s*"({alert_name}[^"]+)""",
    """Severity=({alert_severity}[^\s]+)""",
    """Policy=({alert_type}.+?)\s+\w+=""",
    """userEmail=({email_address}[^\s]+)""",
    """action=({result}.+?)\s+\w+=""",
    """usage=({alert_type}.+?)\s+\w+=""",
    """usageIp=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
    """usageApplication=({process_path}({process_dir}(?:(\w+:)?[^:]+)?[\\\/])?({process_name}.+?))\s+\w+="""
  ]
  ParserVersion = "v1.0.0"


}
```