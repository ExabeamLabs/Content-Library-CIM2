#### Parser Content
```Java
{
Name = zscaler-ia-csv-endpoint-login-success-signin
  ParserVersion = "v1.0.0"
  Vendor = Zscaler
  Product = Zscaler Internet Access
  TimeFormat = "dd MMM yyyy HH:mm:ss"
  Conditions = [ """,Sign In,""", """,Successful,""", """,Login,""" ]
  Fields = [
    """({time}\d\d \w+ \d\d\d\d \d\d:\d\d:\d\d)""",
    """({event_name}Sign In),({dest_host}[^,]+),({result}Successful),({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?,({additional_info}[^,]+),({operation}Login),"""
  ]


}
```