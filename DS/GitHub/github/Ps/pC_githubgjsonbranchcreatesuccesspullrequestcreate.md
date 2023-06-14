#### Parser Content
```Java
{
Name = github-g-json-branch-create-success-pullrequestcreate
  ParserVersion = "v1.0.0"
  Conditions = [ """"action":"pull_request.create"""", """"operation_type":"create"""" ]
  Fields = ${GithubParsersTemplates.json-github-actions.Fields} [
    """"pull_request_title":"({additional_info}[^"]+)"""
    """"pull_request_url":"({url}[^"]+)"""
  ]      
  DupFields = [ "object->repository" ]

json-github-actions = {
    Vendor = GitHub
    Product = GitHub
    TimeFormat = "epoch"
    Fields = [
      """"@timestamp":({time}\d{13})""",
      """"action":"({operation}[^"]+)""",
      """"transport_protocol_name":"({protocol}[^"]+)""",
      """"user_agent":"({user_agent}[^"]+)""",
      """"actor_ip":"({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
      """"repo":"({object}[^"]+)""",
      """"actor":"({user}[^"]+)""",
      """"user":"({user}[^"]+)""",
      """"operation_type":"({operation_type}[^"]+)""",
      """({app}(?i)github)"""
    
}
```