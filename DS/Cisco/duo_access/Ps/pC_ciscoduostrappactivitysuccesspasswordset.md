#### Parser Content
```Java
{
Name = cisco-duo-str-app-activity-success-passwordset
  Conditions = [ """ duo: """, """|activation_set_password|""" ]
  ParserVersion = "v1.0.0"

duo-app-activity = {
  Vendor = Cisco
  Product = Duo Access
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Fields = [
    """({time}\d\d\d\d-\d\d-\d\d \d\d:\d\d:\d\d)""",
    """:\d\d\|({full_name}[^\|]*)\|(|(({dest_user}[\w\.\-\!\#\^\~]{1,40}\$?)|({dest_user_full_name}\w+(\s+\w+)+)))\|({operation}[^\|]+)\|""",
    """"email":\s*"({email_address}[^@"]+@({email_domain}[^"\s]+))"""",
    """({app}duo)"""
  
}
```