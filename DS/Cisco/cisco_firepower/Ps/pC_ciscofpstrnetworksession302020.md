#### Parser Content
```Java
{
Name = cisco-fp-str-network-session-302020
  ParserVersion = "v1.0.0"
  Vendor = Cisco
  Product = Cisco Firepower
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Conditions = [ """%FTD-""", """-302020""", """ Built """, """ ICMP connection for """ ]
  Fields = [
    """({host}[\w\-.]+)\s*:\s*%FTD-""",
    """%FTD-({priority}\d+)-({event_code}\d+)""",
    """({event_name}Built ({direction}inbound|outbound) ({protocol}ICMP) connection)""",
    """Built outbound ICMP.*?faddr\s+((({dest_ip}(\d{1,3}\.){3}\d{1,3}|([A-Fa-f0-9%.]*:[A-Fa-f0-9%.:]+(th0)?))|({dest_host}[^\s]+?))((\/({dest_port}\d+))|\s+)|({icmp_seq_num}\S+))""",
    """Built inbound ICMP.*?faddr\s+((({src_ip}(\d{1,3}\.){3}\d{1,3}|([A-Fa-f0-9%.]*:[A-Fa-f0-9%.:]+(th0)?))|({src_host}[^\s]+?))((\/({src_port}\d+)\s+)|\s+)|({icmp_seq_num}\S+))""",
    """Built outbound ICMP.*?laddr\s+(({src_ip}(\d{1,3}\.){3}\d{1,3}|([A-Fa-f0-9%.]*:[A-Fa-f0-9%.:]+(th0)?))|({src_host}[^\s]+?))((\/({src_port}\d+)(\(|\s+))|\s+)""",
    """Built inbound ICMP.*?laddr\s+(({dest_ip}(\d{1,3}\.){3}\d{1,3}|([A-Fa-f0-9%.]*:[A-Fa-f0-9%.:]+(th0)?))|({dest_host}[^\s]+?))((\/({dest_port}\d+)(\(|\s+))|\s+)""",
    """gaddr\s+((({dest_translated_ip}(\d{1,3}\.){3}\d{1,3}|([A-Fa-f0-9%.]*:[A-Fa-f0-9%.:]+(th0)?))|({dest_translated_host}[^\s]+?))((\/({dest_translated_port}\d+)(\(|\s+))|\s+)|(\S+))""" # cmp_type is removed
  ]


}
```