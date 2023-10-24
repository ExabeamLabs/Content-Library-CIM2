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
  """({result}AuthAttempt) ({host}[\w\-.]+) \[({time}\d+\/\w+\/\d\d\d\d:\d\d:\d\d:\d\d [+-]\d+)\] \"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))? ({user}[\w\.\-]{1,40}\$?)\" \"({app}.+?) \S+ ({resource}[^\"\s]+)""""
]
ParserVersion = "v1.0.0"


}
```