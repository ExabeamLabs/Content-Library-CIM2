#### Parser Content
```Java
{
Name = cisco-ie-str-email-subject
    ParserVersion = v1.0.0
    Vendor = Cisco
    Product = IronPort Email
    TimeFormat = "yyyy-MM-dd HH:mm:ss"
    Conditions = [ """MID """, """ Subject """ ]
    Fields = [
      """MID ({alert_id}\d+) Subject '?({email_subject}[^']+?)\s*('|$)"""
    ]
    DupFields = [ "alert_id->message_id" ]
  

}
```