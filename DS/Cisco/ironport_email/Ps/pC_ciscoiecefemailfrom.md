#### Parser Content
```Java
{
Name = cisco-ie-cef-email-from
    ParserVersion = v1.0.0
    Vendor = Cisco
    Product = IronPort Email
    TimeFormat = "epoch"
    Conditions = [ """CEF:""", """MID """, """CID """, """rom""" ]
    Fields = [
      """\sahost=({host}[\w\-\.]+)\s*""",
      """\srt=({time}\d{13})""",
      """MID ({alert_id}\d+)""",
      """(F|f)rom[:'].+?<({email_address}[^@>]+@[^>]+)>""",
      """\sagt=({src_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})\s*"""    
    ]
    DupFields = [ "alert_id->message_id" ]
 

}
```