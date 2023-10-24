#### Parser Content
```Java
{
Name = "microsoft-rras-kv-vpn-logout-success-coid"
Vendor = "Microsoft"
Product = "Microsoft RRAS"
TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
Conditions = [
  """RoutingDomainID-"""
  """CoID= {"""
  """The user with ip address"""
  """has disconnected"""
]
Fields = [
  """CoID=\{({session_id}[^\{\}]+?)\}"""
  """The user with ip address ({src_translated_ip}[a-fA-F\d.:]+)"""
]
ParserVersion = "v1.0.0"


}
```