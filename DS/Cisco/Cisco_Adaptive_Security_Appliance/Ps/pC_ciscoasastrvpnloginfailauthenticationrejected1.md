#### Parser Content
```Java
{
Name = cisco-asa-str-vpn-login-fail-authentication-rejected-1
  ParserVersion = v1.0.0
  Vendor = Cisco
  Product = Cisco Adaptive Security Appliance
  TimeFormat = "MMM dd yyyy HH:mm:ss"
  Conditions = [ """%ASA""" , """-113005""", """ AAA failure """, """server =""" ]
  Fields = [
    """(\s|>)({time}\w+\s+\d\d\s\d{4}\s\d\d:\d\d:\d\d)""",
    """\w+\s+\d+ \d\d:\d\d:\d\d\s+(::ffff:)?({host}\S+)\s*:*\s+%ASA""",
    """\d{4}-\d\d-\d\dT\d\d:\d\d:\d\d.\d+Z\s({host}[^\s<]+)""",
    """server\s*=\s*(::ffff:)?(({dest_ip}[a-fA-F\d.:]{7,})|({dest_host}\S+))""",
    """reason\s*=\s*({failure_reason}[^:=]+?)\s*:""",
    """user\s*=\s*(?:|({user}[^:]+))\s+:""",
    """user IP\s*=\s*(::ffff:)?({src_ip}[a-fA-F\d.:]+)""",
    """%ASA-\d+-({event_code}113005)""",
    """({event_name}AAA user authentication Rejected)"""
 ]


}
```