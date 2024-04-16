#### Parser Content
```Java
{
Name = cisco-ie-str-email-from
    ParserVersion = v1.0.0
    Vendor = Cisco
    Product = IronPort Email
    TimeFormat = "EEE MMM dd HH:mm:ss yyyy"
    Conditions = [ """MID """, """CID """, """from""" ]
    Fields = [
      """({time}\w+ \w+ \d+ \d\d:\d\d:\d\d \d\d\d\d) Info: MID""",
      """MID ({alert_id}\d+)""",
      """(F|f)rom[:']*.+?<({src_email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({src_email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))>"""
    ]
    DupFields = [ "alert_id->message_id" ]
 

}
```