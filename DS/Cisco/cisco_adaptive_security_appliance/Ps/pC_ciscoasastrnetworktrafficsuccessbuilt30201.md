#### Parser Content
```Java
{
Name = cisco-asa-str-network-traffic-success-built-30201
  Vendor = Cisco
  Product = Cisco Adaptive Security Appliance
  ParserVersion = v1.0.0
  TimeFormat = "MMM dd yyyy HH:mm:ss"
  Conditions = [ """%ASA-""", """-30201""", """: Built """, """ connection """]
  Fields = [
    """({time}\w+ \d\d (\d\d\d\d )?\d\d:\d\d:\d\d+)""",
    """(\w{3} (\d\d| \d) (\d\d\d\d )?(\d\d| \d):\d\d:\d\d)\s+(GMT|(::ffff:)?({host}[\w.\-:].+?[^:]))\s*:?\s*%ASA-""",
    """<\d+>(::ffff:)?({host}[\w.\-:].+?[^:])\s+%ASA-""",
    """%ASA-({priority}\d+)-({event_code}\d+)""",
    """({event_name}Built ({direction}inbound|outbound) ({protocol}TCP|UDP) connection)""",
    """\sconnection\s+({connection_id}\d+)\s+for""",
"""Built outbound.*?for\s+({dest_interface}.+?):((::ffff:)?({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4})(:({dest_port}\d+))?|([A-Fa-f0-9%.]*:[A-Fa-f0-9%.:]+(th0)?))|(::ffff:)?({dest_host}[^\s].+?))((\/({dest_port}\d+)\s+)|\s+)\(((::ffff:)?({dest_translated_ip}(\d{1,3}\.){3}\d{1,3}|([A-Fa-f0-9%.]*:[A-Fa-f0-9%.:]+(th0)?))|(::ffff:)?({dest_translated_host}[^\s].+?))(\/({dest_translated_port}\d+))?\)(\(.+?\))?\s+to\s+({src_interface}.+?):((::ffff:)?({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4})(:({src_port}\d+))?|([A-Fa-f0-9%.]*:[A-Fa-f0-9%.:]+(th0)?))|(::ffff:)?({src_host}[^\s].+?))((\/({src_port}\d+)\s+)|\s+)\(((::ffff:)?({src_translated_ip}(\d{1,3}\.){3}\d{1,3}|([A-Fa-f0-9%.]*:[A-Fa-f0-9%.:]+(th0)?))|(::ffff:)?({src_translated_host}[^\s].+?))(\/({src_translated_port}\d+))?\)(\s+\(({user}.+?)\))?""",
"""Built inbound.*?for\s+({src_interface}.+?):((::ffff:)?({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4})(:({src_port}\d+))?|([A-Fa-f0-9%.]*:[A-Fa-f0-9%.:]+(th0)?))|(::ffff:)?({src_host}[^\s].+?))((\/({src_port}\d+)\s+)|\s+)\(((::ffff:)?({src_translated_ip}(\d{1,3}\.){3}\d{1,3}|([A-Fa-f0-9%.]*:[A-Fa-f0-9%.:]+(th0)?))|(::ffff:)?({src_translated_host}[^\s].+?))(\/({src_translated_port}\d+))?\)(\(.+?\))?\s+to\s+({dest_interface}.+?):((::ffff:)?({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4})(:({dest_port}\d+))?|([A-Fa-f0-9%.]*:[A-Fa-f0-9%.:]+(th0)?))|(::ffff:)?({dest_host}[^\s].+?))((\/({dest_port}\d+)\s+)|\s+)\(((::ffff:)?({dest_translated_ip}(\d{1,3}\.){3}\d{1,3}|([A-Fa-f0-9%.]*:[A-Fa-f0-9%.:]+(th0)?))|(::ffff:)?({dest_translated_host}[^\s].+?))(\/({dest_translated_port}\d+))?\)(\s+\(({user}.+?)\))?"""

 ]


}
```