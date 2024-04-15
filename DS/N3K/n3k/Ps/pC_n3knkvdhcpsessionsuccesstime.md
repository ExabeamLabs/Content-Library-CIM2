#### Parser Content
```Java
{
Name = "n3k-n-kv-dhcp-session-success-time"
Vendor = "N3K"
Product = "N3K"
TimeFormat = "epoch_sec"
Conditions = [
  """maskedIP"""
  """_time"""
  """Domain"""
]
Fields = [
  """"_time":\s+"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d\d\d)"""
  """\sinfo_search_time=({time}\d{10}\.\d{3})"""
  """("|\s)Host(":\s+|=)"?({dest_host}[^",]+)"""
  """("|\s)maskedIP(":\s+|=)"({dest_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?"""
  """("|\s)MAC(":\s+|=)"?({src_mac}[^",]+)"""
]
DupFields = [
  "dest_host->user"
]
ParserVersion = "v1.0.0"


}
```