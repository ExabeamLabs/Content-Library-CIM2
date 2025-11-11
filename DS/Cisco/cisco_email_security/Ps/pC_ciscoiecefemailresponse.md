#### Parser Content
```Java
{
Name = cisco-ie-cef-email-response
    ParserVersion = v1.0.0
    Vendor = Cisco
    Product = Cisco Email Security
    TimeFormat = "epoch"
    Conditions = [ """CEF:""", """MID """, """ RID """, """ Response """ ]
    Fields = [
      """\srt=({time}\d{13})""",
      """MID ({message_id}({alert_id}\d+)) ({additional_info}[^"]+?)\s\w+="""
    ]
  

}
```