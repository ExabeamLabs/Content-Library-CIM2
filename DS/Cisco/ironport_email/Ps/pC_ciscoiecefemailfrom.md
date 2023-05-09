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
      """(F|f)rom[:'].+?<({src_email_address}[^@>]+@[^>]+)>""",
      """\sagt=({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))\s*"""    
    ]
    DupFields = [ "alert_id->message_id" ]
 

}
```