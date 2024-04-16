#### Parser Content
```Java
{
Name = airlock-sah-str-app-notification-webrequests
  Vendor = Airlock
  Product = Airlock Security Access Hub
  ParserVersion = v1.0.0
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Conditions = [ """ Web-Requests:""", """rid:""", """sid:""" ]
  Fields = [
    """({host}[\w\-.]+)\s+Web-Requests:""",
# rid is removed
    """sid:({user_sid}[^\s]+)""",
    """ip:({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
# m_value is removed
  ]


}
```