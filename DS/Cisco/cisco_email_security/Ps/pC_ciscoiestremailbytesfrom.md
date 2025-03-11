#### Parser Content
```Java
{
Name = cisco-ie-str-email-bytesfrom
    ParserVersion = v1.0.0
    Vendor = Cisco
    Product = Cisco Email Security
    TimeFormat = "yyyy-MM-dd HH:mm:ss"
    Conditions = [ """MID """, """ ready """, """ bytes from <""" ]
    Fields = [
      """MID ({alert_id}\d+)""",
      """({bytes}\d+) bytes from <({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.-])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)>"""
    ]
    DupFields = [ "alert_id->message_id" ]
  

}
```