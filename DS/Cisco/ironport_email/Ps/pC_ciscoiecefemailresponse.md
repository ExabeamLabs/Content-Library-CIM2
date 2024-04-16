#### Parser Content
```Java
{
Name = cisco-ie-cef-email-response
    ParserVersion = v1.0.0
    Vendor = Cisco
    Product = IronPort Email
    TimeFormat = "epoch"
    Conditions = [ """CEF:""", """MID """, """ RID """, """ Response """ ]
    Fields = [
      """\srt=({time}\d{13})""",
      """MID ({alert_id}\d+) ({additional_info}[^"]+?)\s\w+="""
    ]
    DupFields = [ "alert_id->message_id" ]
  

}
```