#### Parser Content
```Java
{
Name = github-g-kv-http-request-api
  ParserVersion = v1.0.0
  Vendor = GitHub
  Product = GitHub
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
  Conditions = [ """github_unicorn""", """ controller=""","""request_category=api""" ]
  Fields = [
    """\snow="({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)""",
    """({host}\S+)\s+github_unicorn:""",
    """\scurrent_user=(?:nil|({user}[\w\.\-\!\#\^\~]{1,40}\$?))\s+(\w+=|$)""",
    """\suser=(?:nil|({user}[\w\.\-\!\#\^\~]{1,40}\$?))\s+(\w+=|$)""",
    """\srepo=(?:nil|({object}[^\s]+))\s+(\w+=|$)""",
    """\saction=({operation}[^\s]+)\s+(\w+=|$)""",
    """\sremote_address=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
    """\srequest_host=(?:({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?|({dest_host}[^\s]+))\s+(\w+=|$)""",
    """\suser_agent="({user_agent}[^"]+)"""",
    """\suser_agent=({user_agent}[^\s]+)\s+(\w+=|$)""",
    """\sstatus=({http_response_code}\d+)""",
    """({app}github)""",
    """accept=({mime}[^\s]+)"""
  ]


}
```