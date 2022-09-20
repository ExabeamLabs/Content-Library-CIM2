#### Parser Content
```Java
{
Name = cisco-ie-email-outcome
    ParserVersion = v1.0.0
    Vendor = Cisco
    Product = IronPort Email
    TimeFormat = "yyyy-MM-dd HH:mm:ss"
    Conditions = [ """ Message done""", """ MID """, """RID""" ]
    Fields = [
      """({result}done)""",
      """MID ({alert_id}\d+)"""
    ]


}
```