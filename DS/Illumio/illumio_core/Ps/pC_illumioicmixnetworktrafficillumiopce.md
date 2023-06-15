#### Parser Content
```Java
{
Name = illumio-ic-mix-network-traffic-illumiopce
  ParserVersion = v1.0.0
  Vendor = Illumio
  Product = Illumio Core
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ssZ"
  Conditions = [ """ illumio_pce""", """"un":"""", """"src_hostname":"""", """"pce_fqdn":"""" ]
  Fields = [
    """\s+({host}[^\s]+)\s+illumio_pce""",
    """"timestamp":"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\dZ)"""",
    """pid=({process_id}\d+)""",
    """sev=({alert_severity}[^=]+?)\s+\w+=""",
    """"src_ip":"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""",
    """"dst_ip":"({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?"""",
    """"dst_port":({dest_port}\d+)""",
    """"proto":({protocol}\d+)""",
    """"src_hostname":"({src_host}[^"]+)"""",
    """"dst_hostname":"({dest_host}[^"]+)"""",
    """"un":"(({domain}[^\\"]+)\\+)?({user}[^"]+)"""",
    """"fqdn":"({web_domain}[^"]+)"""",
    """"pn":"({process_name}[^"]+)"""",
    """"dir":"({direction}[^"]+)"""",
    """"pd":({result}\d+)""",
    """"dst_href":"({uri_path}[^"]+)""""
  ]


}
```