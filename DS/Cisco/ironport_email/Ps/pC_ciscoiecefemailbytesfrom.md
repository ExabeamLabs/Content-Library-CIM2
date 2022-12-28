#### Parser Content
```Java
{
Name = cisco-ie-cef-email-bytesfrom
    ParserVersion = v1.0.0
    Vendor = Cisco
    Product = IronPort Email
    TimeFormat = "epoch"
    Conditions = [ """CEF:""", """MID """, """ ready """, """ bytes from <""" ]
    Fields = [
      """ahost=({host}[\w\-\.]+)\s*""",
      """\srt=({time}\d{13})""",
      """MID ({alert_id}\d+)""",
      """({bytes}\d+) bytes from <({email_address}[^@>]+@[^>]+)>""",
      """\sduser=({dest_email_address}[^\@]+\@[^\s]+)\s*""",
      """cs6=({email_subject}[^=]+)\s+""",
      """\sagt=({src_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})\s*"""    
    ]
    DupFields = [ "alert_id->message_id" ]
  

}
```