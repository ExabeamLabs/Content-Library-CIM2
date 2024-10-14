#### Parser Content
```Java
{
Name = illumio-ic-json-network-traffic-pce_fqdn
  ParserVersion = v1.0.0
  Vendor = Illumio
  Product = Illumio Core
  ExtractionType = json
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ssZ"
  Conditions = [ """.illum.io""", """"dir":"""", """"pd":""", """"pce_fqdn":"""" ]
  Fields = [
    """exa_json_path=$.dst_labels.severity,exa_field_name=alert_severity"""
    """exa_json_path=$.pce_fqdn,exa_field_name=web_domain"""
    """exa_json_path=$.timestamp,exa_field_name=time"""
    """exa_json_path=$.src_ip,exa_field_name=src_ip"""
    """exa_json_path=$.dst_ip,exa_field_name=dest_ip"""
    """exa_json_path=$.dst_port,exa_field_name=dest_port"""
    """exa_json_path=$.src_port,exa_field_name=src_port"""
    """exa_json_path=$.dst_href,exa_field_name=uri_path"""
    """exa_json_path=$.pd,exa_field_name=result"""
    """exa_json_path=$.dir,exa_field_name=direction"""
    """exa_json_path=$.un,exa_regex=(((?i)NT AUTHORITY|({domain}[^\\=]+))\\+)?((?i)SYSTEM|NETWORK SERVICE|LOCAL SERVICE|({user}[\w\.\-\!\#\^\~]{1,40}\$?))"""
    """exa_json_path=$.pn,exa_field_name=process_name"""
    """exa_json_path=$.dst_hostname,exa_field_name=dest_host"""
    """exa_json_path=$.src_hostname,exa_field_name=src_host"""
    """exa_json_path=$.proto,exa_field_name=protocol"""
    """exa_json_path=$.network,exa_field_name=network"""
  ]
}  

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
    """"un":"(({domain}[^\\"]+)\\+)?({user}[\w\.\-\!\#\^\~]{1,40}\$?)"""",
    """"fqdn":"({web_domain}[^"]+)"""",
    """"pn":"({process_name}[^"]+)"""",
    """"dir":"({direction}[^"]+)"""",
    """"pd":({result}\d+)""",
    """"dst_href":"({uri_path}[^"]+)""""
  ]


}
```