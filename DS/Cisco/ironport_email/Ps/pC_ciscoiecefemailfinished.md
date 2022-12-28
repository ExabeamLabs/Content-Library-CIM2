#### Parser Content
```Java
{
Name = cisco-ie-cef-email-finished
    ParserVersion = v1.0.0
    Vendor = Cisco
    Product = IronPort Email
    TimeFormat = "epoch"
    Conditions = [ """CEF:""", """Message finished MID """ ]
    Fields = [
      """\sahost=({host}[\w\-\.]+)\s*""",
      """\sagt=({src_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})\s*""",
      """\srt=({time}\d{13})""",
      """Message finished MID ({alert_id}\d+) ({result}[^=]+?)("|\s+\w+(=)?|\s*$)"""
    ]
    DupFields = [ "alert_id->message_id" ]
  

}
```