#### Parser Content
```Java
{
Name = cisco-cc-str-alert-trigger-success-voice_ha
  Vendor = Cisco
  Product = Cisco Collaboration
  ParserVersion = v1.0.0
  TimeFormat = ["MMM dd HH:mm:ss.SSS", "MMM d HH:mm:ss.SSS"]
  Conditions = [ """%VOICE_HA-""", """DATA_RECREATE_ERR""", """mainst ID:""", """ CID:""" ]
  Fields = [
    """({time}\w+\s\d{1,2}\s\d+:\d+:\d+\.\d+)""",
    """({sequence}\d+):\s*({host}[\w\-\.]+):\s*({process_id}\d+):""",
    """({event_code}%VOICE_HA-({alert_severity}\d)-({alert_name}[^:]+)):""",
    """%VOICE_HA-\d-[^:]+:\s\(({alert_type}[^\)]+)\)"""
    """mainst ID:({alert_id}\d+)""",
    """%VOICE_HA-\d-[^:]+:\s*({additional_info}[^$]+)\s*$""",
    """%VOICE_HA-\d-([^:]+:){2}\s*({error_info}[^$]+)\s*$"""
  ]


}
```