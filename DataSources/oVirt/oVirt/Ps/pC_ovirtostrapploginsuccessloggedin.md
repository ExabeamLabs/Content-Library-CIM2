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
    """USER_VDC_LOGIN.+? User (?:({email_address}[^\s@]+@({email_domain}[^\s@]+))\S*|({user}[^\s]+)) connecting from '({src_ip}[A-Fa-f:\d.]+)""",
    """({app}ovirt)"""
  ]


}
```