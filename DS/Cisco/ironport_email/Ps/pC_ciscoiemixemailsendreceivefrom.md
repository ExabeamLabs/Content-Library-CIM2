#### Parser Content
```Java
{
Name = cisco-ie-mix-email-send-receive-from
    Vendor = Cisco
    Product = IronPort Email
	  ParserVersion = v1.0.0
    TimeFormat = ["epoch","MMM dd HH:mm:ss"]
    Conditions = [ """ MID """, """ ICID """, """ From:""" ]
    Fields = [
      """({time}\w{3}\s\d\d\s\d\d:\d\d:\d\d)\s[\w\_]+:""",
      """\srt=({time}\d{13})""",
      """MID ({alert_id}\d+)""",
      """(F|f)rom[:'].+?<({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.-])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)>""",
    ]
    DupFields = [ "alert_id->message_id" ]
  

}
```