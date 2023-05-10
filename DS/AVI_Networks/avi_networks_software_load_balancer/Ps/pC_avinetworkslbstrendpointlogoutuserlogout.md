#### Parser Content
```Java
{
Name = avinetworks-lb-str-endpoint-logout-userlogout
  ParserVersion = v1.0.0
  Vendor = AVI Networks
  Product = AVI Networks Software Load Balancer
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Conditions = [ """Avi-Controller:""", """event USER_LOGOUT occurred""", """logout from""" ]
  Fields = [
    """At\s({time}\d\d\d\d-\d\d-\d\d\s\d\d:\d\d:\d\d)""",
    """User\s({user}[^\s]+)""",
    """from\s({src_ip}[a-fA-F\d\.:]+)\.\s+""",
    """event\s({event_name}USER_LOGOUT)""",
    """object\s({object}[^\s]+)""",
  ]


}
```