#### Parser Content
```Java
{
Name = microsoft-evsecurity-csv-network-close-success-4655
  Vendor = Microsoft
  Product = Event Viewer - Security
  ParserVersion = v1.0.0
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
  Conditions = [ """(4655)""", """[WIN]""", """Microsoft-Windows-Security-Auditing""" ]
  Fields = [
    """:\d\d\s+({host}.+?)\s*EvntSLog""",
    """({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)""",
    """\(({event_code}\d+)\)""",
    """({event_category}Microsoft-Windows-Security-Auditing)""",
    """({event_name}An IPsec main mode security association ended)""",
    """Local Network Address:\s*({src_ip}[^\s]+)\s""",
    """Remote Network Address:\s*({dest_ip}[^\s]+)\s""",
  ]


}
```