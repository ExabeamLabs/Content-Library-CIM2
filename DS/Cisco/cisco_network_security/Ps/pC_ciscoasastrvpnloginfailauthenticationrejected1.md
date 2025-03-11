#### Parser Content
```Java
{
Name = cisco-asa-str-vpn-login-fail-authentication-rejected-1
  ParserVersion = v1.0.0
  Vendor = Cisco
  Product = Cisco Network Security
  TimeFormat = "MMM dd yyyy HH:mm:ss"
  Conditions = [ """%ASA""" , """-113005""", """ AAA failure """, """server =""" ]
  Fields = [
    """(\s|>)({time}\w+\s+\d\d\s\d{4}\s\d\d:\d\d:\d\d)""",
    """\w+\s+\d+ \d\d:\d\d:\d\d\s+(::ffff:)?({host}\S+)\s*:*\s+%ASA""",
    """\d{4}-\d\d-\d\dT\d\d:\d\d:\d\d.\d+Z\s({host}[^\s<]+)""",
    """server\s*=\s*(::ffff:)?(({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?|({dest_host}\S+))""",
    """reason\s*=\s*({failure_reason}[^:=]+?)\s*:""",
    """user\s*=\s*(?:|\*+|({email_address}[^@:]+@[^\.]+\.[^:]+)|({user}[\w\.\-\!\#\^\~]{1,40}\$?)@({domain}[^:\.@]+)|(({=domain}[^\\\/:]+)[\\\/]+)?({=user}[^:]+))\s+:""",
    """user IP\s*=\s*(::ffff:)?({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
    """%(FTD|ASA)(-\w+)?-\d+-({event_code}113005)""",
    """({event_name}AAA user authentication Rejected)"""
 ]


}
```