#### Parser Content
```Java
{
Name = cisco-ie-cef-email-spam
    ParserVersion = v1.0.0
    Vendor = Cisco
    Product = IronPort Email
    TimeFormat = "epoch"
    Conditions = [ """CEF:""", """MID """, """CASE spam""" ]
    Fields = [
      """\sahost=({host}[\w\-\.]+)\s*""",
      """\srt=({time}\d+)""",
      """MID ({alert_id}\d+)""",
      """CASE spam ({spam_score}.+?)(\s+\w+=|\s*$)""",
      """\sagt=({src_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})\s*"""
    ]
    DupFields = [ "alert_id->message_id" ]
  

}
```