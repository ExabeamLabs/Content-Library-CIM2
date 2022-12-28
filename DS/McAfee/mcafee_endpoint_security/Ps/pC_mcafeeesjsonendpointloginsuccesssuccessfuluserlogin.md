#### Parser Content
```Java
{
Name = mcafee-es-json-endpoint-login-success-successfuluserlogin
  Vendor = McAfee
  Product = McAfee Endpoint Security
  ParserVersion = "v1.0.0"
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Conditions = [ """ATD""" , """"Action": "Successful user login"""" ]
  Fields = [
    """<\d+>\S+ \d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d(\+|\-)\d\d:\d\d ({host}\S+)""",
    """"Action":\s*"({event_code}[^"]+)""",
    """"User":\s*"({user}[^"]+)""",
    """"UserID":\s*"({user_id}[^"]+)""",
    """"Timestamp":\s*"({time}\d\d\d\d-\d\d-\d\d \d\d:\d\d:\d\d)""",
    """"Client":\s*"({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
    """"HTTPAgent":\s*"({user_agent}[^"]+)""",
  ]


}
```