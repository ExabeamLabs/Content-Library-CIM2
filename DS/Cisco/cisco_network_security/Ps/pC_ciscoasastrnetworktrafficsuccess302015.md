#### Parser Content
```Java
{
Name = cisco-asa-str-network-traffic-success-302015
  ParserVersion = v1.0.0
  Vendor = Cisco
  Product = Cisco Network Security
  TimeFormat = ["MMM dd yyyy HH:mm:ss", "yyyy-MM-dd'T'HH:mm:ss.SSSZ"]
  Conditions = [ """%ASA-""", """-302015""", """: Built outbound """, """ connection """]
  Fields = [
    """({time}\d{4}\-\d{2}\-\d{2}T\d{2}:\d{2}:\d{2}\.\d+((\+|\-)\d\d:\d\d)?)\s+""",
"""\s(({host}[\w.\-]+))\s+([-\s:]+)?%ASA""",
    """({time}\w{1,3}\s\d{1,2}\s\d\d\d\d\s\d\d:\d\d:\d\d)""",
    """\s\d\d:\d\d:\d\d\s({host}[\w\-.]+)?\s*:\s*%ASA""",
    """%ASA-({priority}\d+)-({event_code}\d+)""",
    """({event_name}Built ({direction}outbound) ({protocol}TCP|UDP) connection)""",
    """\sconnection\s+({connection_id}\d+)\s+for""",
    """Built outbound[^\n]+?for\s+({dest_interface}[^:]+):((::ffff:)?({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4})|([A-Fa-f0-9]*:[A-Fa-f0-9:]+(th0)?))|(::ffff:)?({dest_host}[^\s]+?))((\/({dest_port}\d+)\s+)|\s+)\(((::ffff:)?({dest_translated_ip}(\d{1,3}\.){3}\d{1,3}|([A-Fa-f0-9]*:[A-Fa-f0-9:]+(th0)?))|(::ffff:)?({dest_translated_host}[^\s]+?))(\/({dest_translated_port}\d+))?\)\s+to\s+({src_interface}[^:]+):((::ffff:)?({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4})|([A-Fa-f0-9]*:[A-Fa-f0-9:]+(th0)?))|(::ffff:)?({src_host}[^\s]+?))((\/({src_port}\d+)\s+)|\s+)\(((::ffff:)?({src_translated_ip}(\d{1,3}\.){3}\d{1,3}|([A-Fa-f0-9]*:[A-Fa-f0-9:]+(th0)?))|(::ffff:)?({src_translated_host}[^\s]+?))(\/({src_translated_port}\d+))?\)(\((({email_address}([A-Za-z0-9]+[!#$%&'+-\/=?^_`~])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)|({user}[\w\.\-\!\#\^\~]{1,40}\$?))\))?"""
  ]


}
```