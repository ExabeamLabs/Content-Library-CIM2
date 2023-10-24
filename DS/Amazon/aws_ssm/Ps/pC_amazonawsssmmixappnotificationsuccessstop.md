#### Parser Content
```Java
{
Name = amazon-awsssm-mix-app-notification-success-stop
  ParserVersion = "v1.0.0"
  Vendor = Amazon
  Product = AWS SSM
  TimeFormat = "epoch"
  Conditions = [ """CEF:""", """requestClientApplication=AWS_SSM""", """System Logging Service""", """]: Stop""", """systemd[""" ]
  Fields = [
    """end=({time}\d{13})\s""",
    """\s\d\d:\d\d:\d\d\s({host}[\w\-\.]+)\s""",
    """systemd\[\d+\]:\s({event_name}[^"\.]+)"""
  ]


}
```