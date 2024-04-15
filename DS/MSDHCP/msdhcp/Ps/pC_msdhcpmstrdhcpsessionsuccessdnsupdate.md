#### Parser Content
```Java
{
Name = "msdhcp-m-str-dhcp-session-success-dnsupdate"
Vendor = "MSDHCP"
Product = "MSDHCP"
TimeFormat = "yyyy-MM-dd'T'HH:mm:ssZ"
Conditions = [
  """[][]"""
  """[DHCP]"""
  """ MSDHCP """
  """,DNS Update Successful,"""
]
Fields = [
  """\[\]\[\]\[({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?\]\[({event_code}\d+)\]\[DHCP\]"""
  """({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d(\+|\-)\d\d:\d\d)\s+({host}[\w.\-]+)"""
  """"([^,]*,)\d+\/\d+\/\d+,\d+:\d+:\d+,({operation}[^,]+),(|({dest_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?),(|({dest_host}[\w\-.]+)),(|({dest_mac}[^,\s]+)),"""
]
DupFields = [
  "event_code->service_id"
]
ParserVersion = "v1.0.0"


}
```