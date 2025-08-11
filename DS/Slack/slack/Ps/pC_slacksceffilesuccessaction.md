#### Parser Content
```Java
{
Name = "slack-s-cef-file-success-action"
  Vendor = "Slack"
  Product = "Slack"
  ExtractionType = json
  TimeFormat = ["yyyy-MM-dd'T'HH:mm:ss.SSSZ", "epoch_sec"]
  Conditions = [
     """destinationServiceName =Slack"""
     """"action":""""
  ]
  Fields = [
      """({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d+Z)\s+""",
      """"date_create":({time}\d{10})""",
      """"user":\{[^\}]*?"name":"({full_name}[^"]+)"""
      """"user":\{[^\}]*?"id":"({user_id}[^"]+)"""
      """exa_json_path=$.date_create,exa_regex=({time}\d{10})""",
      """.?destinationServiceName =({app}(s|S)lack)""",
      """exa_regex=destinationServiceName =({app}Slack)""",
      """exa_json_path=$.actor.user.id,exa_field_name=user_id""",
      """exa_json_path=$.actor.user.name,exa_field_name=full_name""",
      """exa_json_path=$.actor.user.email,exa_regex=({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.-])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)""",
      """exa_json_path=$.entity..name,exa_field_name=object""",
      """exa_json_path=$.action,exa_field_name=operation""",
      """exa_json_path=$.context.ip_address,exa_regex=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
      """exa_json_path=$.context.location.domain,exa_field_name=domain""",
      """exa_json_path=$.context.ua,exa_field_name=user_agent""",
      """user":\{"id":"({user_id}[^"]+)","name":"({full_name}[^"]+)"""",
      """"email":"(|({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.-])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+))"""",
      """action":"({operation}[^"]+)""",
      """"ip_address":"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""",
      """"domain":"({domain}[^"]+)"""",
      """"ua":"({user_agent}[^"]+)"""",
      """"entity":.+?"name":"({object}[^"]+)""""
  ]
  ParserVersion = "v1.0.0"


}
```