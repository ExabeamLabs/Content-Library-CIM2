#### Parser Content
```Java
{
Name = cisco-asa-str-vpn-login-fail-authentication-rejected
  ParserVersion = v1.0.0
  Vendor = Cisco
  Product = Cisco Adaptive Security Appliance
  TimeFormat = "MMM dd yyyy HH:mm:ss"
  Conditions = [ """%ASA""" , """-113005""", """ AAA user """ ]
  Fields = [
    """\w+\s+\d+ \d\d:\d\d:\d\d\s+(::ffff:)?({host}\S+)\s*:*\s+%ASA""",
    """(\s|>)({time}\w+ \d\d \d\d\d\d \d\d:\d\d:\d\d)""",
    """reason\s*=\s*({failure_reason}[^;=]+?)\s*:""",
    """server\s*=\s*(::ffff:)?({dest_ip}[a-fA-F\d.:]+)""",
    """user\s*=\s*(?:|({user}[^:]+))\s+:""",
    """user IP\s*=\s*(::ffff:)?({src_ip}[a-fA-F\d.:]+)""",
    """%ASA-\d+-({event_code}113005)""",
    """({event_name}AAA user authentication Rejected)"""
 ]


}
```