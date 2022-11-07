#### Parser Content
```Java
{
Name = ovirt-o-kv-app-logout-success-loggedout
  Vendor = oVirt
  Product = oVirt
  ParserVersion = "v1.0.0"
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Conditions = [ """EVENT_ID: USER_VDC_LOGOUT""", """ovirt""", """logged out""" ]
  Fields = [
    """({time}\d\d\d\d-\d\d-\d\d \d\d:\d\d:\d\d),.+?ovirt""",
    """USER_VDC_LOGOUT.+? User (?:({email_address}[^\s@]+@[^\s@]+)\S*|({user}[^\s]+)) connected from '({src_ip}[A-Fa-f:\d.]+)""",
  ]


}
```