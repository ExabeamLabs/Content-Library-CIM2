#### Parser Content
```Java
{
Name = "workday-wd-cef-endpoint-login-fail-proxyusername"
Vendor = "Workday"
Product = "Workday"
TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
Conditions = [ """"proxyUserName":""", """"authenticationType":""", """"signonIPAddress":""", """"authenticationFailureMessage":""" ]
Fields = [
  """({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)\.\d+Z\s+[\w\-.]+\s+"""
  """authenticationFailureMessage"+:"+({failure_reason}[^"]+)"""
  """userName":"(Invalid Authentication|({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))|({user}[\w\.\-\!\#\^\~]{1,40}\$?)|({full_name}[^\s,]+([\s,]+\s*[^\s"]+)+?))""""
  """signonIPAddress"+:"+({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?"""
  """authenticationType"+:"+({login_type_text}({auth_method}[^"]+))"""
  """dproc=({event_name}[^=]+?)\s+(\w+=|$)"""
  """({app}Workday)"""
]
ParserVersion = "v1.0.0"


}
```