#### Parser Content
```Java
{
Name = cisco-asa-str-network-traffic-success-302015
  ParserVersion = v1.0.0
  Vendor = Cisco
  Product = Cisco Adaptive Security Appliance
  TimeFormat = "MMM dd yyyy HH:mm:ss"
  Conditions = [ """%ASA-""", """-302015""", """: Built outbound """, """ connection """]
  Fields = [
    """({time}\w{1,3}\s\d{1,2}\s\d\d\d\d\s\d\d:\d\d:\d\d)""",
    """\s\d\d:\d\d:\d\d\s({host}[^\s]+)""",
    """%ASA-({priority}\d+)-({event_code}\d+)""",
    """({event_name}Built ({direction}outbound) ({protocol}TCP|UDP) connection)""",
    """\sconnection\s+({connection_id}\d+)\s+for""",
    """Built outbound[^\n]+?for\s+({dest_interface}[^:]+):((::ffff:)?({dest_ip}(\d{1,3}\.){3}\d{1,3}|([A-Fa-f0-9]*:[A-Fa-f0-9:]+(th0)?))|(::ffff:)?({dest_host}[^\s]+?))((\/({dest_port}\d+)\s+)|\s+)\(((::ffff:)?({dest_translated_ip}(\d{1,3}\.){3}\d{1,3}|([A-Fa-f0-9]*:[A-Fa-f0-9:]+(th0)?))|(::ffff:)?({dest_translated_host}[^\s]+?))(\/({dest_translated_port}\d+))?\)\s+to\s+({src_interface}[^:]+):((::ffff:)?({src_ip}(\d{1,3}\.){3}\d{1,3}|([A-Fa-f0-9]*:[A-Fa-f0-9:]+(th0)?))|(::ffff:)?({src_host}[^\s]+?))((\/({src_port}\d+)\s+)|\s+)\(((::ffff:)?({src_translated_ip}(\d{1,3}\.){3}\d{1,3}|([A-Fa-f0-9]*:[A-Fa-f0-9:]+(th0)?))|(::ffff:)?({src_translated_host}[^\s]+?))(\/({src_translated_port}\d+))?\)(\s+\(({user}[^\)]+)\))?"""
  ]


}
```