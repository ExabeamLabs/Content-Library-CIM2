#### Parser Content
```Java
{
Name = "sophos-utm-kv-network-traffic-ulogd"
  ParserVersion = "v1.0.0"
  Vendor = "Sophos"
  Product = "Sophos UTM"
  TimeFormat = "yyyy:MM:dd-HH:mm:ss"
  Conditions = [
""" ulogd["""
""" sub="""
""" action="""
  ]
  Fields = [
"""({time}\d+:\d+:\d+-\d+:\d+:\d+)"""
"""ulogd\[({event_id}\d+)"""
"""action=\"({result}[^\"]+)"""
"""fwrule=\"({rule_id}\d+)"""
"""srcmac=\"({src_mac}[^\"]+)"""
"""dstmac=\"({dest_mac}[^\"]+)"""
"""srcip=\"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
"""dstip=\"({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?"""
"""proto=\"({protocol}[^\"]+)"""
"""srcport=\"({src_port}\d+)"""
"""dstport=\"({dest_port}\d+)"""
"""initf=\"({src_interface}[^\"]+)"""
"""outitf=\"({dest_interface}[^\"]+)"""
"""length=\"({bytes}\d+)"""
"""name=\"({event_name}[^\"]+)"""
"""severity=\"({alert_severity}[^\"]+)"""
  ]


}
```