#### Parser Content
```Java
{
Name = "microsoft-rras-kv-vpn-logout-success-disconnected"
Vendor = "Microsoft"
Product = "Microsoft RRAS"
TimeFormat = "MM/dd/yyyy' at 'H:mm a"
Conditions = [
  """RoutingDomainID-"""
  """CoID= {"""
  """ and disconnected on """
  """The reason for disconnecting was"""
]
Fields = [
  """CoID=\{({session_id}[^\{\}]+?)\}"""
  """:\s*The user (({domain}[^\\\/]+)[\\\/]+)?({user}[^\\\/]+?)\s+connected on port"""
  """\sand disconnected on ({time}\d+/\d+/\d\d\d\d at \d+:\d+ (am|AM|pm|PM))"""
  """The user was active for ({session_min}\d+) minutes ({session_sec}\d+) seconds"""
  """({bytes_out}\d+) bytes were sent and ({bytes_in}\d+) bytes were received"""
  """\sThe reason for disconnecting was ({result_reason}[^\.]+)"""
]
ParserVersion = "v1.0.0"


}
```