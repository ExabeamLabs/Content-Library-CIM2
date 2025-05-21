#### Parser Content
```Java
{
Name = kemp-loadmaster-str-app-logout-success-loggedout
  Vendor = Kemp
  Product = Kemp LoadMaster
  ParserVersion = "v1.0.0"
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Conditions = [ """logger: User""", """ Logged out """ ]
  Fields = [
    """User\s+({user}[\w\.\-\!\#\^\~]{1,40}\$?)\s+\(({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
    """({event_name}Logged out)""",
    """({event_category}logger)"""
  ]


}
```