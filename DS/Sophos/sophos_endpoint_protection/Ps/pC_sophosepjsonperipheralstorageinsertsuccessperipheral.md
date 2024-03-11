#### Parser Content
```Java
{
Name = sophos-ep-json-peripheral-storage-insert-success-peripheral
  Vendor = Sophos
  Product = Sophos Endpoint Protection
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
  Conditions = [ """"Event::Endpoint::Device::""", """"name": "Peripheral """ ]
  Fields = [
    """"rt":\s*"({time}\d\d\d\d\-\d\d\-\d\dT\d\d:\d\d:\d\d\.\d\d\dZ)""",
    """"name":\s*"({operation}[^":]+):\s({device_type}[^"]+)""",
    """"name":\s*"({operation_details}[^"]+)""",
    """"dhost":\s*"({src_host}[^"]+)""",
    """"suser":\s*"(?:n\/a|({full_name}[^"\\,]+))"""",
    """"suser":\s*"(n\/a|({last_name}[^",\\\s]+),\s*({first_name}[^,"\\\s]+))""",
    """"suser":\s*"(?:n\/a|({user}[^"]+))"""",
    """"suser":\s*"(({domain}[^\\",]+)\\+)?({user}[^",\\\/\s]+)"""",
    """"id":\s*"({device_id}[^"]+)""",
  ]
  ParserVersion = "v1.0.0"


}
```