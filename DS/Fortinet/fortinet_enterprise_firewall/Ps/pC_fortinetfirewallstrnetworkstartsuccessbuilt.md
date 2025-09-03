#### Parser Content
```Java
{
Name = fortinet-firewall-str-network-start-success-built
  Vendor = Fortinet
  Product = Fortinet Enterprise Firewall
  TimeFormat = "MMM dd HH:mm:ss"
  Conditions = [ """ Built """, """ connection """, """for """ ]
  Fields = [
    """({time}\w{3}\s+\d{1,2}\s+\d\d:\d\d:\d\d)\s""",
    """\s({host}[\w\-.]+)\sBuilt """,
    """({action}Built) ({direction}\w+) ({protocol}[^\s]+) connection""",
    """Built outbound.*?for\s+({dest_interface}.+?):({dest_ip}(\d{1,3}\.){3}\d{1,3}|([A-Fa-f0-9%.]*:[A-Fa-f0-9%.:]+(th0)?))((\/({dest_port}\d+)\s+)|\s+)\(({dest_translated_ip}(\d{1,3}\.){3}\d{1,3}|([A-Fa-f0-9%.]*:[A-Fa-f0-9%.:]+(th0)?))(\/({dest_translated_port}\d+))?\)\s+to\s+({src_interface}.+?):({src_ip}(\d{1,3}\.){3}\d{1,3}|([A-Fa-f0-9%.]*:[A-Fa-f0-9%.:]+(th0)?))((\/({src_port}\d+)\s+)|\s+)\(({src_translated_ip}(\d{1,3}\.){3}\d{1,3}|([A-Fa-f0-9%.]*:[A-Fa-f0-9%.:]+(th0)?))(\/({src_translated_port}\d+))?\)""",
    """Built inbound.*?for\s+({src_interface}.+?):({src_ip}(\d{1,3}\.){3}\d{1,3}|([A-Fa-f0-9%.]*:[A-Fa-f0-9%.:]+(th0)?))((\/({src_port}\d+)\s+)|\s+)\(({src_translated_ip}(\d{1,3}\.){3}\d{1,3}|([A-Fa-f0-9%.]*:[A-Fa-f0-9%.:]+(th0)?))(\/({src_translated_port}\d+))?\)\s+to\s+({dest_interface}.+?):({dest_ip}(\d{1,3}\.){3}\d{1,3}|([A-Fa-f0-9%.]*:[A-Fa-f0-9%.:]+(th0)?))((\/({dest_port}\d+)\s+)|\s+)\(({dest_translated_ip}(\d{1,3}\.){3}\d{1,3}|([A-Fa-f0-9%.]*:[A-Fa-f0-9%.:]+(th0)?))(\/({dest_translated_port}\d+))?\)""",
    """Built outbound.*?faddr\s+({dest_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})(\/({dest_port}\d+))?""",
    """Built inbound.*?faddr\s+({src_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})(\/({src_port}\d+))?""",
    """Built outbound.*?laddr\s+({src_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})\/(({src_port}\d+))?""",
    """Built inbound.*?laddr\s+({dest_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})\/(({dest_port}\d+))?"""
  ]
  ParserVersion = "v1.0.0"


}
```