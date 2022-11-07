#### Parser Content
```Java
{
Name = cisco-ie-kv-email-alert
  ParserVersion = v1.0.0
  Vendor = Cisco
  Product = IronPort Email
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Conditions = [ """ MID """, """ From=""", """To=""", """Subject=""" ]
  Fields = [
    """\WFrom=[^<]+<({email_address}[^@]+@[^>,]+)""",
    """To=({dest_email_address}[^=]+?)(,|\s+$)""",
    """Subject=({email_subject}.+?)(,\s+\w+=|\s*$)""",
    """RemoteIP=({dest_ip}[A-Fa-f.:\d]+)""",
    """MID ({alert_id}\d+)"""
  ]


}
```