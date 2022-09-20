#### Parser Content
```Java
{
Name = microsoft-rras-kv-authentication-success-authsuccess
  ParserVersion = v1.0.0
  Vendor = Microsoft
  Product = Routing and Remote Access Service
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
  Conditions = [ """RoutingDomainID-""", """CoID= {""", """has connected and has been successfully authenticated""" ]
  Fields = [
    """CoID=\{({session_id}[^\{\}]+?)\}""",
    """:\s*The user (({domain}[^\\\/]+?)[\\\/]+)?({user}[^\\\/]+?) has connected""",
    ]


}
```