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
    """\scurrent_user=(?:nil|({user}[^\s]+))\s+(\w+=|$)""",
    """\suser=(?:nil|({user}[^\s]+))\s+(\w+=|$)""",
    """\srepo=(?:nil|({object}[^\s]+))\s+(\w+=|$)""",
    """\saction=({operation}[^\s]+)\s+(\w+=|$)""",
    """\sremote_address=({src_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})""",
    """\srequest_host=(?:({dest_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})|({dest_host}[^\s]+))\s+(\w+=|$)""",
    """\suser_agent="({user_agent}[^"]+)"""",
    """\suser_agent=({user_agent}[^\s]+)\s+(\w+=|$)""",
    """\sstatus=({http_response_code}\d+)""",
    """({app}github)""",
    """accept=({mime}[^\s]+)"""
  ]


}
```