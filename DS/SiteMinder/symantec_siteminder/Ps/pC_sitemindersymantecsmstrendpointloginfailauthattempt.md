#### Parser Content
```Java
{
Name = "siteminder-symantecsm-str-endpoint-login-fail-authattempt"
Vendor = "SiteMinder"
Product = "Symantec SiteMinder"
TimeFormat = "dd/MMM/yyyy:HH:mm:ss Z"
Conditions = [
  """AuthAttempt """
  """ ["""
  """] """"
]
Fields = [
  """({result}AuthAttempt)\s+({host}[\w\-.]+)\s+\[({time}\d+\/\w+\/\d\d\d\d:\d\d:\d\d:\d\d [+-]\d+)\]\s+"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?\s+.*?((CN|cn)|((({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))|(({user}[\w\.\-\!\#\^\~\@\[\`]{1,40}\$?)|({full_name}[\w\s]+)|))\")\s+\"(({app}[^\s]+)\s+\S+\s+(({resource}({uri_path}[^"\s\?]+)({uri_query}\?[^"]+)*))))"""
]
ParserVersion = "v1.0.0"


}
```