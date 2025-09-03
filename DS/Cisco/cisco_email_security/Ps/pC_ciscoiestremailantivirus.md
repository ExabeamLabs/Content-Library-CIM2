#### Parser Content
```Java
{
Name = cisco-ie-str-email-antivirus
    ParserVersion = v1.0.0
    Vendor = Cisco
    Product = Cisco Email Security
    TimeFormat = "epoch"
    Conditions = [ """MID """, """ antivirus """ ]
    Fields = [
      """MID ({alert_id}\d+)""",
      """ antivirus ({malware_score}.+?)(\s+\w+=|\s*$)"""
      """ antivirus -[^-]*?- Result '({malware_score}.+?)'"""
    ]
    DupFields = [ "alert_id->message_id" ]
  

}
```