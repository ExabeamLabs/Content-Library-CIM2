#### Parser Content
```Java
{
Name = cisco-asa-str-network-notification-success
  Vendor = Cisco
  Product = Cisco Adaptive Security Appliance
  ParserVersion = v1.0.0
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Conditions = [ """%ASA-""" ]
  Fields = [
    """({time}\w+ \d+ \d+ \d\d:\d\d:\d\d)\s*(::ffff:)?({host}[\w\-.]+)?\s*:\s%ASA""",
    """\w+ \d+ \d\d:\d\d:\d\d (::ffff:)?({host}\d{1,3}.\d{1,3}.\d{1,3}.\d{1,3}) %ASA""",
    """(::ffff:)?({host}[\w\-.]+)\s+({time}\w+ \d\d \d\d\d\d \d\d:\d\d:\d\d):\s*%ASA""",
    """%ASA-({priority}\d+)-({event_code}\d+)""",
    """from ((::ffff:)?({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4})(:({src_port}\d+))?|([A-Fa-f0-9%.]*:[A-Fa-f0-9%.:]+(th0)?))|(::ffff:)?\(?({src_host}[^\)\s].+?)\)?) to ((::ffff:)?({dest_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4})(:({dest_port}\d+))?|([A-Fa-f0-9%.]*:[A-Fa-f0-9%.:]+(th0)?))|(::ffff:)?({dest_host}[^\s]+?)),.*? on interface ({dest_interface}\S+)"""",
    """ from (WLC-LAN_|VENDOR-DMZ_Vlan_601:)?(inside:|outside:)?((::ffff:)?({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4})|([A-Fa-f0-9%.]*:[A-Fa-f0-9%.:]+(th0)?))|(::ffff:)?\(?({src_host}[^\)\s].+?)\)?)((\/({src_port}\d+)\s+)|\s+)to ({dest_interface}\S+?)\s*:\s*((::ffff:)?({dest_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4})|([A-Fa-f0-9%.]*:[A-Fa-f0-9%.:]+(th0)?))|(::ffff:)?({dest_host}[^\s].+?))((\/({dest_port}\d+))|\s+)""",
    """ src ({src_interface}\S+?)\s*:\s*((::ffff:)?({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4})(:({src_port}\d+))?|([A-Fa-f0-9%.]*:[A-Fa-f0-9%.:]+(th0)?))|(::ffff:)?\(?({src_host}[^\)\s].+?)\)?) dst ({dest_interface}\S+?)\s*:\s*((::ffff:)?({dest_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4})(:({dest_port}\d+))?|([A-Fa-f0-9%.]*:[A-Fa-f0-9%.:]+(th0)?))|(::ffff:)?({dest_host}[^\s].+?))""",
    """%ASA-\d+-\d+:\s*({event_name}[^:].+?)\s+from (WLC-LAN_)?({src_interface}[^\s:]+):\s*((::ffff:)?({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4})|([A-Fa-f0-9%.]*:[A-Fa-f0-9%.:]+(th0)?))|(::ffff:)?\(?({src_host}[^\)\s].+?)\)?)(\/({src_port}\d+))?.+?to ({dest_interface}[^\s:]+):\s*((::ffff:)?({dest_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4})|([A-Fa-f0-9%.]*:[A-Fa-f0-9%.:]+(th0)?))|(::ffff:)?({dest_host}[^\s].+?))(\/({dest_port}\d+))""",
    """(Teardown|Built) local-host ([^\s]+|INSIDE|Outside|outside):((::ffff:)?({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4})(:({src_port}\d+))?|([A-Fa-f0-9%.]*:[A-Fa-f0-9%.:]+(th0)?))|(::ffff:)?\(?({src_host}[^\)\s].+?)\)?)($|\s)"""
    """URL Server (::ffff:)?({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4})) not responding""",
    """({protocol}ICMP|TCP|UDP)"""
  ]


}
```