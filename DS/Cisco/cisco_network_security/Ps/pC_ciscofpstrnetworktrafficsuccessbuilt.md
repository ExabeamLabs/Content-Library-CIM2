#### Parser Content
```Java
{
Name = "cisco-fp-str-network-traffic-success-built"
  ParserVersion = "v1.0.0"
  Vendor = "Cisco" 
  Product = Cisco Network Security
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Conditions = [
"""%FTD-"""
"""-30201"""
""": Built """
""" connection """
  ]
  Fields = [
"""\s(({host}[\w.\-]+))\s+([-\s:]+)?%FTD"""
"""%FTD-({priority}\d+)-({event_code}\d+)"""
"""({event_name}Built ({direction}inbound|outbound) ({protocol}TCP|UDP) connection)"""
"""\sconnection\s+({connection_id}\d+)\s+for"""
"""Built outbound.*?for\s+({dest_interface}.+?):(({dest_ip}(\d{1,3}\.){3}\d{1,3}|([A-Fa-f0-9%.]*:[A-Fa-f0-9%.:]+(th0)?))|({dest_host}[^\s]+?))((\/({dest_port}\d+)\s+)|\s+)\((({dest_translated_ip}(\d{1,3}\.){3}\d{1,3}|([A-Fa-f0-9%.]*:[A-Fa-f0-9%.:]+(th0)?))|({dest_translated_host}[^\s]+?))(\/({dest_translated_port}\d+))?\)(\(.+?\))?\s+to\s+({src_interface}.+?):(({src_ip}(\d{1,3}\.){3}\d{1,3}|([A-Fa-f0-9%.]*:[A-Fa-f0-9%.:]+(th0)?))|({src_host}[^\s]+?))((\/({src_port}\d+)\s+)|\s+)\((({src_translated_ip}(\d{1,3}\.){3}\d{1,3}|([A-Fa-f0-9%.]*:[A-Fa-f0-9%.:]+(th0)?))|({src_translated_host}[^\s]+?))(\/({src_translated_port}\d+))?\)(\s+\((({email_address}[^@\s\)]+@[^\.\)\s]+\.[^\s\)]+)|({user}[\w\.\-\!\#\^\~]{1,40}\$?))\))?"""
"""Built inbound.*?for\s+({src_interface}.+?):(({src_ip}(\d{1,3}\.){3}\d{1,3}|([A-Fa-f0-9%.]*:[A-Fa-f0-9%.:]+(th0)?))|({src_host}[^\s]+?))((\/({src_port}\d+)\s+)|\s+)\((({src_translated_ip}(\d{1,3}\.){3}\d{1,3}|([A-Fa-f0-9%.]*:[A-Fa-f0-9%.:]+(th0)?))|({src_translated_host}[^\s]+?))(\/({src_translated_port}\d+))?\)(\(.+?\))?\s+to\s+({dest_interface}.+?):(({dest_ip}(\d{1,3}\.){3}\d{1,3}|([A-Fa-f0-9%.]*:[A-Fa-f0-9%.:]+(th0)?))|({dest_host}[^\s]+?))((\/({dest_port}\d+)\s+)|\s+)\((({dest_translated_ip}(\d{1,3}\.){3}\d{1,3}|([A-Fa-f0-9%.]*:[A-Fa-f0-9%.:]+(th0)?))|({dest_translated_host}[^\s]+?))(\/({dest_translated_port}\d+))?\)(\s+\((({email_address}[^@\s\)]+@[^\.\)\s]+\.[^\s\)]+)|({user}[\w\.\-\!\#\^\~]{1,40}\$?))\))?"""
  ]


}
```