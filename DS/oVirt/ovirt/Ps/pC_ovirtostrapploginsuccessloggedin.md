#### Parser Content
```Java
{
Name = ovirt-o-str-app-login-success-loggedin
  ParserVersion = v1.0.0
  Vendor = oVirt
  Product = oVirt
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Conditions = [ """EVENT_ID: USER_VDC_LOGIN""", """ovirt""", """logged in""" ]
  Fields = [
    """({time}\d\d\d\d-\d\d-\d\d \d\d:\d\d:\d\d),.+?ovirt""",
    """USER_VDC_LOGIN.+? User (?:({email_address}[^\s@]+@({email_domain}[^\s@]+))\S*|({user}[\w\.\-\!\#\^\~]{1,40}\$?)) connecting from '({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
    """({app}ovirt)"""
    """({operation}USER_VDC_LOGIN)"""
  ]


}
```