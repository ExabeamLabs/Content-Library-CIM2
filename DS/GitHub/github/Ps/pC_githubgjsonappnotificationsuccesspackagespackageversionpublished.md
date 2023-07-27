#### Parser Content
```Java
{
Name = github-g-json-app-notification-success-packagespackageversionpublished
  ParserVersion = "v1.0.0"
  Conditions = [ """"action":"packages.package_version_published"""", """"operation_type":"create"""" ]
  Fields = ${GithubParsersTemplates.json-github-actions.Fields} [
    """"ecosystem":"({additional_info}[^"]+)"""
    """"package":"({object}[^"]+)"""
  ]    

json-github-actions = {
    Vendor = GitHub
    Product = GitHub
    TimeFormat = "epoch"
    Fields = [
      """"@timestamp":({time}\d{13})""",
      """"action":"({operation}[^"]+)""",
      """"transport_protocol_name":"({protocol}[^"]+)""",
      """"user_agent":"({user_agent}[^"]+)""",
      """"actor_ip":"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
      """"repo":"({object}[^"]+)""",
      """"actor":"({user}[\w\.\-]{1,40}\$?)""",
      """"user":"({user}[\w\.\-]{1,40}\$?)""",
      """"operation_type":"({operation_type}[^"]+)""",
      """({app}(?i)github)"""
    
}
```