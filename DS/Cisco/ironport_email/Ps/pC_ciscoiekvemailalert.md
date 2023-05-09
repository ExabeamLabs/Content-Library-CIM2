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
    """\WFrom=[^<]+<({src_email_address}[^@]+@[^>,]+)""",
    """To=({dest_email_address}[^=]+?)(,|\s+$)""",
    """Subject=({email_subject}.+?)(,\s+\w+=|\s*$)""",
    """RemoteIP=({dest_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?""",
    """MID ({alert_id}\d+)"""
  ]


}
```