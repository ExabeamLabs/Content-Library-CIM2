#### Parser Content
```Java
{
Name = cisco-ie-str-email-attachment
    ParserVersion = v1.0.0
    Vendor = Cisco
    Product = IronPort Email
    TimeFormat = "yyyy-MM-dd HH:mm:ss"
    Conditions = [ """MID """, """ attachment """ ]
    Fields = [
      """MID ({alert_id}\d+) attachment '({email_attachment}[^']+)'""",
      """attachment '({email_attachment}[^']+\.({file_ext}[^']+))'""",
       ]
    DupFields = [ "alert_id->message_id" 
    "email_attachment->attachment" 
    ]
  

}
```