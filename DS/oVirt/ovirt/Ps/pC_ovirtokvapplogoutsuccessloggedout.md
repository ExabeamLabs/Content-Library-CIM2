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
    """USER_VDC_LOGOUT.+? User (?:({email_address}[^\s@]+@[^\s@]+)\S*|({user}[\w\.\-]{1,40}\$?)) connected from '({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
  ]


}
```