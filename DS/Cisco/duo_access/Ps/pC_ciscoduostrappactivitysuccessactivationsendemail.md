#### Parser Content
```Java
{
Name = cisco-duo-str-app-activity-success-activationsendemail
  Conditions = [ """ duo: """, """|activation_send_email|""" ]
  ParserVersion = "v1.0.0"

duo-app-activity = {
  Vendor = Cisco
  Product = Duo Access
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Fields = [
    """({time}\d\d\d\d-\d\d-\d\d \d\d:\d\d:\d\d)""",
    """:\d\d\|({full_name}[^\|]*)\|(|({dest_user}[^\|]+))\|({operation}[^\|]+)\|""",
    """"email":\s*"({email_address}[^@"]+@({email_domain}[^"\s]+))"""",
    """({app}duo)"""
  
}
```