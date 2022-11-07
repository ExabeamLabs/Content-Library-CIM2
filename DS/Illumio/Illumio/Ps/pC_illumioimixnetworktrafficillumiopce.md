#### Parser Content
```Java
{
Name = illumio-i-mix-network-traffic-illumiopce
  ParserVersion = v1.0.0
  Vendor = Illumio
  Product = Illumio
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ssZ"
  Conditions = [ """ illumio_pce""", """"un":"""", """"src_hostname":"""", """"pce_fqdn":"""" ]
  Fields = [
    """\s+({host}[^\s]+)\s+illumio_pce""",
    """"timestamp":"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\dZ)"""",
    """pid=({process_id}\d+)""",
    """sev=({alert_severity}[^=]+?)\s+\w+=""",
    """"src_ip":"({src_ip}[A-Fa-f\d:.]+)"""",
    """"dst_ip":"({dest_ip}[A-Fa-f\d:.]+)"""",
    """"dst_port":({dest_port}\d+)""",
    """"proto":({protocol}\d+)""",
    """"src_hostname":"({src_host}[^"]+)"""",
    """"dst_hostname":"({dest_host}[^"]+)"""",
    """"un":"(({domain}[^\\"]+)\\{1,20})?({user}[^"]+)"""",
    """"fqdn":"({web_domain}[^"]+)"""",
    """"pn":"({process_name}[^"]+)"""",
    """"dir":"({direction}[^"]+)"""",
    """"pd":({result}\d+)""",
    """"dst_href":"({uri_path}[^"]+)""""
  ]


}
```