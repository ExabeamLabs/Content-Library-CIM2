#### Parser Content
```Java
{
Name = github-g-kv-app-activity-success-githubunicorn
  ParserVersion = v1.0.0
  Vendor = GitHub
  Product = GitHub
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSSSSZ"
  Conditions = [ """service.name="github-unicorn"""", """code.function""" ]
  Fields = [
    """\sTimestamp="({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d.\d\d\d\d\d\dZ)""",
    """({host}\S+)\s+github-unicorn""",
    """\sgh.actor.login="(?:nil|({user}[\w\.\-\!\#\^\~]{1,40}\$?))"""",
    """\shttp.client_ip="({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
    """user_agent="({user_agent}[^"]+)"""",
    """\sgh.context.url="({url}[^"]+)""",
    """\sservice.name="({service_name}[^"]+)""",
    """\scode.namespace="({additional_info}[^"]+)""",
    """\scode.function="({operation}[^"]+)""",
    """({app}github)"""
  ]


}
```