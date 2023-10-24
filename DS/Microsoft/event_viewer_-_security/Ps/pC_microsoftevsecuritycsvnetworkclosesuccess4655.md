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
    """Local Network Address:\s*({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?\s""",
    """Remote Network Address:\s*({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?\s""",
  ]


}
```