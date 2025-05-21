#### Parser Content
```Java
{
Name = "ovirt-o-str-app-login-fail-unabletologin"
Vendor = "oVirt"
Product = "oVirt"
TimeFormat = "yyyy-MM-dd HH:mm:ss"
Conditions = [
  """Unable to log in."""
  """ovirt"""
]
Fields = [
  """({time}\d\d\d\d-\d\d-\d\d \d\d:\d\d:\d\d),.+?ovirt"""
  """Cannot authenticate user '({user}[\w\.\-\!\#\^\~]{1,40}\$?)(@({domain}[^\s]+))?' connecting from '({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
  """({app}ovirt)"""
]
ParserVersion = "v1.0.0"


}
```