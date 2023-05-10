#### Parser Content
```Java
{
Name = cisco-cwc-str-endpoint-login-success-loginpassed
  Vendor = Cisco
  Product = Catalyst Wireless Controller
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Conditions = [ """ %WEBSERVER-5-LOGIN_PASSED: """, """ Login Successful """ ]
  Fields = [
    """Login Successful from host ({src_ip}[A-Fa-f\d:.]+) by user '(({email_address}[^@]+@[^']+)|({user_id}\d+)|({user}[^']+))'""",
    """%({event_name}WEBSERVER-5-LOGIN_PASSED):"""
  ]
  ParserVersion = "v1.0.0"


}
```