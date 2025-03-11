#### Parser Content
```Java
{
Name = cisco-ie-cef-email-finished
    ParserVersion = v1.0.0
    Vendor = Cisco
    Product = Cisco Email Security
    TimeFormat = "epoch"
    Conditions = [ """CEF:""", """Message finished MID """ ]
    Fields = [
      """\sahost=({host}[\w\-\.]+)\s*""",
      """\sagt=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))\s*""",
      """\srt=({time}\d{13})""",
      """Message finished MID ({alert_id}\d+) ({result}[^=]+?)("|\s+\w+(=)?|\s*$)"""
    ]
    DupFields = [ "alert_id->message_id" ]
  

}
```