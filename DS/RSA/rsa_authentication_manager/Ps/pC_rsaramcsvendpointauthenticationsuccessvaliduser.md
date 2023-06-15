#### Parser Content
```Java
{
Name = rsa-ram-csv-endpoint-authentication-success-validuser
  Vendor = RSA
  Product = RSA Authentication Manager
  TimeFormat = "yyyy-MM-dd HH:mm:ss:SSS zzz"
  Conditions = [ """,Authentication Success,Valid User,""" ]
  Fields = [
    """({time}\d\d\d\d-\d\d-\d\d\s+\d\d:\d\d:\d\d:\d+\s+\w+)""",
    """\s\d\d:\d\d:\d\d:\d+[^,]+\,([^,]*\,){3}(\s*|({user}[^,\s]+))\,([^,]*\,){6}(\s*|({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?)\,(\s*|({=src_port}\d+))\,(\s*|({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?)\,""",
    """({event_name}Authentication Success)""",
    """({result}Success)"""
  ]
  ParserVersion = "v1.0.0"


}
```