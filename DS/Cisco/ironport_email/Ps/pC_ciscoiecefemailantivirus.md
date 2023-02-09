#### Parser Content
```Java
{
Name = cisco-ie-cef-email-antivirus
    ParserVersion = v1.0.0
    Vendor = Cisco
    Product = IronPort Email
    TimeFormat = "epoch"
    Conditions = [ """CEF:""", """MID """, """ antivirus """ ]
    Fields = [
      """ahost=({host}[\w\-\.]+)\s*""",
      """\srt=({time}\d{13})""",
      """MID ({alert_id}\d+)""",
      """ antivirus ({malware_score}.+?)(\s+\w+=|\s*$)""",
      """ antivirus -[^-]*?- Result '({malware_score}.+?)'""",
      """\sagt=({src_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})\s*"""
    ]
    DupFields = [ "alert_id->message_id" ]
  

}
```