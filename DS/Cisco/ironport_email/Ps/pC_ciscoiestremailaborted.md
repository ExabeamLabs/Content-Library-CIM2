#### Parser Content
```Java
{
Name = cisco-ie-str-email-aborted
    ParserVersion = v1.0.0
    Vendor = Cisco
    Product = IronPort Email
    TimeFormat = "yyyy-MM-dd HH:mm:ss"
    Conditions = [ """Message aborted MID """ ]
    Fields = [
      """\srt=({time}\d+)""",
      """Message ({result}aborted) MID ({alert_id}\d+) Receiving ({failure_reason}.+?)"*(\s+\w+=|\s*$)"""
      """\sMID\s+({alert_id}\d+)\s+({failure_reason}.+?)$"""
      """\sMessage\s+({result}aborted)"""
      """\sMID\s+({alert_id}\d+)"""
    ]
    DupFields = [ "alert_id->message_id" ]
  

}
```