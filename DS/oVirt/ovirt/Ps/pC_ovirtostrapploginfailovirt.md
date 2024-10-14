#### Parser Content
```Java
{
Name = "ovirt-o-str-app-login-fail-ovirt"
Vendor = "oVirt"
Product = "oVirt"
TimeFormat = "yyyy-MM-dd HH:mm:ss"
Conditions = [
  """EVENT_ID: USER_VDC_LOGIN_FAILED"""
  """ovirt"""
  """failed to log in"""
]
Fields = [
  """({time}\d\d\d\d-\d\d-\d\d \d\d:\d\d:\d\d),.+?ovirt"""
  """USER_VDC_LOGIN_FAILED.+? User (({user}[\w\.\-\!\#\^\~]{1,40}\$?)(@({domain}[^@\s]+))?).+connecting from '({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
  """({app}ovirt)"""
  """({operation}USER_VDC_LOGIN_FAILED)"""
]
ParserVersion = "v1.0.0"


}
```