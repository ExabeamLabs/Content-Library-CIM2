#### Parser Content
```Java
{
Name = cisco-ie-str-app-notification-maillogs
  ParserVersion = "v1.0.0"
  Vendor = Cisco
  Product = Cisco Email Security
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Conditions = [ """ mail_logs""", """ Info: """, """ DCID """ ]
  Fields = [
    """\d\d:\d\d:\d\d mail_logs.*: Info: ({event_name}[^\n]+?)\s*$""",
  ]


}
```