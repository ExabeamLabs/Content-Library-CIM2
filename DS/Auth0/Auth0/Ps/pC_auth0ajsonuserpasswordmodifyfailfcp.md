#### Parser Content
```Java
{
Name = auth0-a-json-user-password-modify-fail-fcp
  Conditions = [ """"type":"fcp"""", """"user_id"""", """"client_name"""", """"client_id"""" ]
  Fields=${Auth0AAParsersTemplates.auth0-authentication-template.Fields}[
    """"({operation_type}fcp)"""",
  ]
  ParserVersion = "v1.0.0"
  DupFields = [ "user->dest_user" ]

auth0-authentication-template = {
    Vendor = Auth0
    Product = Auth0
    TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
    Fields = [
      """date"+:"+({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d.\d\d\dZ)""",
      """hostname"+:"+({host}[^"]+)""",
      """description"+:"+({additional_info}[^"]+)\s*"+""",
      """"+ip"+:"+({src_ip}[\da-fA-F.:]+)""",
      """user_name"+:"+(({email_address}[^"@]+@[^"@]+)|({user}[^"]+))"+,""",     
      """user_id"+:"+((({auth_type}[^|"]+)\|({domain}[^|"]+)\|({user}[\w-]+))|(({=auth_type}[^|"]+)\|({=user}[\w-]+)))"""
      """client_name"+:"+({app}[^"]+)""",
      """user_agent"+:"+({user_agent}[^"]+)""",         
      """severity"+:"+({alert_severity}[^"]+)""", 
    
}
```