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
    """server\s*=\s*(::ffff:)?({dest_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?""",
    """user\s*=\s*(({email_address}[^@\s:]+@[^@\s":]+)|((\*+?)|({user}[^@:\s"]+)@({domain}[^:\.@"\s]+)|(({=domain}[^\\\/:\s"]+)[\\\/]+)?({=user}[^"\s:]+)))\s+:""",
    """user IP\s*=\s*(::ffff:)?({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
    """%ASA-\d+-({event_code}113005)""",
    """({event_name}AAA user (authentication|authorization) Rejected)"""
 ]


}
```