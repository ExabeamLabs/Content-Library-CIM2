#### Parser Content
```Java
{
Name = sophos-ep-cef-app-notification-success-updatefailure
  ParserVersion = "v1.0.0"
  Product = Sophos Endpoint Protection
  Conditions = [ """CEF:""", """|sophos|sophos central|""", """Event::Endpoint::UpdateFailure""" ]

cef-sophos-events = {
  Vendor = Sophos
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
  Fields = [
    """rt=({time}\d\d\d\d\-\d\d\-\d\dT\d\d:\d\d:\d\d\.\d\d\dZ)""",
    """dhost=({src_host}[\w\-.]+)""",
    """suser=(?:n\/a|(({domain}[^\\]+?)\\)?({user}[^\s,]+))\s+\w+=""",
    """suser=(n\/a|({full_name}({last_name}[^,\\\s]+),\s*({first_name}[^,\\\s]+)))""",
    """\Wid=({alert_id}[^\s]+)""",
    """source_info_ip=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
    """CEF:([^\|]*\|){4}({alert_type}[^\|]+)""",
    """CEF:([^\|]*\|){5}({alert_name}[^\|]+)""",
    """CEF:([^\|]*\|){6}({alert_severity}[^\|]+)""",
  
}
```