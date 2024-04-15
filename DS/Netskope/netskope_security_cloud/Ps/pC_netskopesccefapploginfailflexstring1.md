#### Parser Content
```Java
{
Name = "netskope-sc-cef-app-login-fail-flexstring1"
Vendor = "Netskope"
Product = "Netskope Security Cloud"
TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
Conditions = [
  """flexString1=Login Failed"""
  """destinationServiceName =Netskope"""
]
Fields = [
  """\Wend=({time}\d+)"""
  """\"+created_at\"+:\"+({time}\d\d\d\d\-\d\d\-\d\dT\d\d:\d\d:\d\d)"""
  """\"time\"\s*:\s*\"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)"""
  """\ssrc=({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
  """\ssuser=({user}[^@\s]+)\s+(\w+=|$)"""
  """\ssuser=({email_address}[^\s@]+@[^\s@]+)\s+(\w+=|$)"""
  """\ssuser=.*?@([\.\w+]+\.)?({email_domain}[^\.\s]+\.(?:com|net|info|edu|org|gov|co|jp|ru|de|ir|it|in|fr|info|pl|nl|es|gr|cz|eu|tv|me|jp|ca|cn|uk|my|cc|id|us|nz|biz|club|io|gg|fi|au|st|tw|asia|sg|ie|li|za|ch))\s+"""
  """\"+created_by\"+:\{.+?\"+name\"+:\"+({full_name}[^\"]+)\"+"""
  """\"+source\"+:\{.+?\"+name\"+:\"+({full_name}[^\"]+)\"+"""
  """\"failureReason\":\"({failure_reason}[^\"]+)\""""
  """\sreason=({failure_reason}.+?)(\s+\w+=|\s*$)"""
  """(\||\s)requestClientApplication=({app}.+?)(\s+\w+=|\s*$)"""
]
DupFields = [
  "app->event_subtype"
]
ParserVersion = "v1.0.0"


}
```