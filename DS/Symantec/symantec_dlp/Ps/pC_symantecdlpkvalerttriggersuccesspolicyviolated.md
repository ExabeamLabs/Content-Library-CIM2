#### Parser Content
```Java
{
Name = symantec-dlp-kv-alert-trigger-success-policyviolated
  Vendor = Symantec
  Product = Symantec DLP
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Conditions = [ """Endpoint Name:""","""Endpoint Server:""", """Policy Violated:""" ]
  Fields = [
    """Message\s*=\s*The user\s* (?:[^\\]+\\)?({user}[\w\.\-]{1,40}\$?)\s*has""",
    """\d\d:\d\d:\dd\s*({host}[^\s]+)""",
    """\s*Endpoint Name:\s*({dest_host}[^\s]+)""",
    """\s*Endpoint IP:\s*\(({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?""",
    """\s*filename:\s*({file_name}[^,]+)""",
    """\s*dir:\s*({file_dir}.+?)\s*Device Instance ID:""",
    """\s*Device Instance ID:\s*({device_id}.+?)\s+(\w+=|$)""",
    """\s*Policy Violated:\s*({alert_name}.+?),\s*Date""",
    """\s*Protocol:\s*({alert_type}.+?),\s*Count""",
    """incident ID:\s*({alert_id}\d+)""",
    """Blocked:\s*({action}.+?)\s*Device Instance ID:"""
  ]
  ParserVersion = "v1.0.0"


}
```