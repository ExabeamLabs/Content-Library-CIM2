#### Parser Content
```Java
{
Name = sophos-ep-cef-app-notification-success-updatesuccess
  ParserVersion = "v1.0.0"
  Product = Sophos Endpoint Protection
  Conditions = [ """CEF:""", """|sophos|sophos central|""", """Event::Endpoint::UpdateSuccess""" ]

cef-sophos-events = {
  Vendor = Sophos
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
  Fields = [
    """rt=({time}\d\d\d\d\-\d\d\-\d\dT\d\d:\d\d:\d\d\.\d\d\dZ)""",
    """dhost=({src_host}[\w\-.]+)""",
    """suser=(?:n\/a|(({domain}[^\\]+?)\\)?({user}[^\s,]+))\s+\w+=""",
    """suser=(n\/a|({full_name}({last_name}[^,\\\s]+),\s*({first_name}[^,\\\s]+)))""",
    """\Wid=({alert_id}[^\s]+)""",
    """source_info_ip=({src_ip}[A-Fa-f:\d.]+)""",
    """CEF:([^\|]*\|){4}({alert_type}[^\|]+)""",
    """CEF:([^\|]*\|){5}({alert_name}[^\|]+)""",
    """CEF:([^\|]*\|){6}({alert_severity}[^\|]+)""",
  
}
```