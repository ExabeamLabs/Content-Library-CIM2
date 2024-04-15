#### Parser Content
```Java
{
Name = "slack-s-cef-file-success-action"
  Vendor = "Slack"
  Product = "Slack"
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
  Conditions = [
     """destinationServiceName =Slack"""
     """"action":""""
  ]
  Fields = [
      """({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d+Z)\s+""",
      """\WdestinationServiceName =({app}Slack)""",
      """user":\{"id":"({user_id}[^"]+)","name":"({full_name}[^"]+)"""",
      """"email":"(|({email_address}[^@]+@({email_domain}[^"]+?)))"""",
      """action":"({operation}[^"]+)""",
      """"ip_address":"({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""",
      """"entity":\{"[^"]+":"[^"]+","[^"]+":\{("[^"]+":"[^"]+",){2}"name":"({object}[^"]+)"""",
      """"domain":"({domain}[^"]+)"""",
  ]
  ParserVersion = "v1.0.0"


}
```