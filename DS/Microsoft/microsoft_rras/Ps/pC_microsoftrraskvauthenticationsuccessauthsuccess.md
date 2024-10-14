#### Parser Content
```Java
{
Name = microsoft-rras-kv-authentication-success-authsuccess
  ParserVersion = v1.0.0
  Vendor = Microsoft
  Product = Microsoft RRAS
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
  Conditions = [ """RoutingDomainID-""", """CoID= {""", """has connected and has been successfully authenticated""" ]
  Fields = [
    """CoID=\{({session_id}[^\{\}]+?)\}""",
    """:\s*The user (({email_address}([A-Za-z0-9]+[!#$%&'+-\/=?^_`~])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+))|({user}[\w\.\-\!\#\^\~]{1,40}\$?)) has connected""",
    ]


}
```