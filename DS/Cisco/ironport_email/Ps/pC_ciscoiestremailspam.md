#### Parser Content
```Java
{
Name = cisco-ie-str-email-spam
    ParserVersion = v1.0.0
    Vendor = Cisco
    Product = IronPort Email
    TimeFormat = "yyyy-MM-dd HH:mm:ss"
    Conditions = [ """MID """, """CASE spam""" ]
    Fields = [
      """MID ({alert_id}\d+)""",
      """CASE spam ({spam_score}.+?)"(\s+\w+=|\s*$)"""
    ]
    DupFields = [ "alert_id->message_id" ]
  

}
```