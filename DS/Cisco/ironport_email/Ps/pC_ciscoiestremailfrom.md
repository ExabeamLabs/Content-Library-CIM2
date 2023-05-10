#### Parser Content
```Java
{
Name = cisco-ie-str-email-from
    ParserVersion = v1.0.0
    Vendor = Cisco
    Product = IronPort Email
    TimeFormat = "EEE MMM dd HH:mm:ss yyyy"
    Conditions = [ """MID """, """CID """, """rom""" ]
    Fields = [
      """({time}\w+ \w+ \d+ \d\d:\d\d:\d\d \d\d\d\d) Info: MID""",
      """MID ({alert_id}\d+)""",
      """(F|f)rom[:']*.+?<({sender}[^@>]+@[^>]+)>"""
    ]
    DupFields = [ "alert_id->message_id" ]
 

}
```