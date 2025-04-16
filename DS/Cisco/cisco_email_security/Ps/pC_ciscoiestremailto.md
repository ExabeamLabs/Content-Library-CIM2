#### Parser Content
```Java
{
Name = cisco-ie-str-email-to
    ParserVersion = v1.0.0
    Vendor = Cisco
    Product = Cisco Email Security
    TimeFormat = "EEE MMM dd HH:mm:ss yyyy"
    Conditions = [ """MID """, """ RID """, """ To: """ ]
    Fields = [
      """({time}\w+ \w+ \d+ \d\d:\d\d:\d\d \d\d\d\d) Info: MID""",
      """MID ({alert_id}\d+) .*? To: <({dest_email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({dest_email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))>""",
    ]
    DupFields = [ "alert_id->message_id" ]
 

}
```