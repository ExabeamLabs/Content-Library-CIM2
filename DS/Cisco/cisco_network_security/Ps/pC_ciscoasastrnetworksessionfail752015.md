#### Parser Content
```Java
{
Name = cisco-asa-str-network-session-fail-752015
  ParserVersion = v1.0.0
  Vendor = Cisco
  Product = Cisco Network Security
  TimeFormat = ["MMM dd yyyy HH:mm:ss", "MMM dd HH:mm:ss"]
  Conditions = [ """-752015""", """Tunnel Manager has failed to establish an L2L SA.""" ]
  Fields = [
    """((::ffff:)?({host}[\w\-.]+)\s+)?({time}\w+ \d\d (\d\d\d\d )?\d\d:\d\d:\d\d)\s*\S*\s*:\s*%\w+-({priority}\d+)""",
    """({event_code}752015)""",
    """({event_name}Tunnel Manager has failed to establish an L2L SA)""",
    """({protocol}IKE)""",
    """%\w+[\w-]+?:\s*({failure_reason}[^=]+?).\s[\w\s]+?=""",
    """\w{3}\s+\d+\s+(\d+\s+)?\d+:\d+:\d+\s+(\d+|({host}[\w\-\.]+))\s"""
  ]


}
```