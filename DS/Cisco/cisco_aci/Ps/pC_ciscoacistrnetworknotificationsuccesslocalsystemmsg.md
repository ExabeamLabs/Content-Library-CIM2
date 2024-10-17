#### Parser Content
```Java
{
Name = cisco-aci-str-network-notification-success-localsystemmsg
    Vendor = Cisco
    Product = Cisco ACI
    ParserVersion = "v1.0.0"
    TimeFormat = "MMM dd HH:mm:ss"
    Conditions = [ """%LOG_LOCAL7-""", """-SYSTEM_MSG""" ]
    Fields = [
      """({time}\w{3}\s+\d+\s+\d+\:\d+\:\d+)\s+({src_host}[\w\-.]+)\s""", 
      """\s({alert_name}%LOG_LOCAL7-\d-SYSTEM_MSG)\s+\[[^\]]+\]\[({action}[^\]]+)\]\[({operation}\w+)\]\[({severity}\w+)\]\[[^\]]+\]\s+({additional_info}({system_type}Tacacs+).+\d+\s({result}unreachable)?)""",
      """\[({action}FSM\:[^\]]+)\]:\s+({additional_info}[^,]+)"""
      """\s({alert_name}%LOG_LOCAL7-\d-SYSTEM_MSG)\s+\[[^\]]+\]\[({action}[^\]]+)\]\[({severity}\w+)\]\[[\w\/\[\]\-\d]+\]\s+({additional_info}[^,]+)""",
    ]


}
```