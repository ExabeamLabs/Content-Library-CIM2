#### Parser Content
```Java
{
Name = cisco-ie-cef-email-from
    ParserVersion = v1.0.0
    Vendor = Cisco
    Product = Cisco Email Security
    TimeFormat = "epoch"
    Conditions = [ """CEF:""", """CISCO|IronPort""", """MID """, """CID """, """rom""" ]
    Fields = [
      """\sahost=({host}[\w\-\.]+)\s*""",
      """\srt=({time}\d{13})""",
      """MID ({alert_id}\d+)""",
      """(F|f)rom[:'].+?<({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.-])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)>""",
      """\sagt=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))\s*""",
     ]
    DupFields = [ "alert_id->message_id" ]
 

}
```