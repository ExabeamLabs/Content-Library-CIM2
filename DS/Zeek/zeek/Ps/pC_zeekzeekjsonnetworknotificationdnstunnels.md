#### Parser Content
```Java
{
Name = "zeek-zeek-json-network-notification-dnstunnels"
  Vendor = "Zeek"
  Product = "Zeek"
  ParserVersion = "v1.0.0"
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSSSSZ"
  Conditions = [ """"_path":"generic_dns_tunnels""",""""dns_client":"""", """"domain":"""", """"generic_dns_tunnels""""]
  Fields = [
    """"ts":"({time}\d\d\d\d-\d{1,2}-\d{1,2}T\d{1,2}:\d{1,2}:\d{1,2}\.\d+Z)"""",
    """"_system_name":"({host}[\w\-.]+)"""",
    """"domain":"({domain}[^"]+)"""",
    """"bytes":({bytes}\d+)""",
# dns_client is removed
  ]


}
```