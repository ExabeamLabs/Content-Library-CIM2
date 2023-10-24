#### Parser Content
```Java
{
Name = sophos-ep-cef-peripheral-storage-insert-success-peripherals
Vendor = "Sophos"
Product = "Sophos Endpoint Protection"
TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
Conditions = [
  """|sophos|sophos central|"""
  """|Event::Endpoint::Device::AlertedOnly|"""
  """group=PERIPHERALS"""
  """|Peripheral allowed:"""
]
Fields = [
  """\Wrt=({time}\d\d\d\d\-\d\d\-\d\dT\d\d:\d\d:\d\d\.\d\d\dZ)"""
  """CEF:([^\|]*\|){5}({operation}[^:\|]+):\s({device_type}[^\|]+)"""
  """CEF:([^\|]*\|){5}({operation_details}[^\|]+)"""
  """\Wdhost=({src_host}[\w\-.]+)\s+(\w+=|$)"""
  """\Wsuser=((({dest_host}[^\s\\]+)\\+)({user}[\w\.\-]{1,40}\$?)|(n\/a|({full_name}[^\\]+?)))\s+(\w+=|$)"""
  """\Wid=({device_id}[^\s]+)"""
]
ParserVersion = "v1.0.0"


}
```