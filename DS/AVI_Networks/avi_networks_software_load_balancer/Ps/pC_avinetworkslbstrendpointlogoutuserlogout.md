#### Parser Content
```Java
{
Name = avinetworks-lb-str-endpoint-logout-userlogout
  ParserVersion = v1.0.0
  Vendor = AVI Networks
  Product = Avi Networks Software Load Balancer
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Conditions = [ """Avi-Controller:""", """event USER_LOGOUT occurred""", """logout from""" ]
  Fields = [
    """At\s({time}\d\d\d\d-\d\d-\d\d\s\d\d:\d\d:\d\d)""",
    """User\s({user}[\w\.\-]{1,40}\$?)""",
    """from\s({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?\.\s+""",
    """event\s({event_name}USER_LOGOUT)""",
    """object\s({object}[^\s]+)""",
  ]


}
```