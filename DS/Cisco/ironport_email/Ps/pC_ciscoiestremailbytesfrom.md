#### Parser Content
```Java
{
Name = cisco-ie-str-email-bytesfrom
    ParserVersion = v1.0.0
    Vendor = Cisco
    Product = IronPort Email
    TimeFormat = "yyyy-MM-dd HH:mm:ss"
    Conditions = [ """MID """, """ ready """, """ bytes from <""" ]
    Fields = [
      """MID ({alert_id}\d+)""",
      """({bytes}\d+) bytes from <({sender}[^@>]+@[^>]+)>"""
    ]
    DupFields = [ "alert_id->message_id" ]
  

}
```