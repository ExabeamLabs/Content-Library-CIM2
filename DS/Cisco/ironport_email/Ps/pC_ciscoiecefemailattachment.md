#### Parser Content
```Java
{
Name = cisco-ie-cef-email-attachment
    ParserVersion = v1.0.0
    Vendor = Cisco
    Product = IronPort Email
    TimeFormat = "epoch"
    Conditions = [ """CEF""", """CISCO|IronPort""", """MID """, """ attachment """ ]
    Fields = [
	  """\srt=({time}\d{13})""",
      """MID ({alert_id}\d+) attachment '({email_attachment}[^']+)'""",
      """attachment '({email_attachment}[^']+\.({file_ext}[^']+))'"""
    ]
    DupFields = [ "alert_id->message_id" ]
  

}
```