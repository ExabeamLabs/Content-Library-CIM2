#### Parser Content
```Java
{
Name = cisco-cwc-str-endpoint-login-success-loginpassed
  Vendor = Cisco
  Product = Cisco IOS
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Conditions = [ """ %WEBSERVER-5-LOGIN_PASSED: """, """ Login Successful """ ]
  Fields = [
    """Login Successful from host ({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))? by user '(({email_address}[^@]+@[^']+)|({user_id}\d+)|({user}[^']+))'""",
    """%({event_name}WEBSERVER-5-LOGIN_PASSED):"""
  ]
  ParserVersion = "v1.0.0"


}
```