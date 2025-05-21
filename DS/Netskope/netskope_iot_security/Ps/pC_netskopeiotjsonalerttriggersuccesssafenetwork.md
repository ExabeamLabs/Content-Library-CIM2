#### Parser Content
```Java
{
Name = netskope-iot-json-alert-trigger-success-safenetwork
  ParserVersion = v1.0.0
  Conditions = [""""packet_alerts":""", """"category":"Not a best practice for a safe network"""", """"signature":"""", """"title":"""" ]

json-netskope-iot-events = {
  Vendor = Netskope
  Product = Netskope IoT Security
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ssZ"
  ExtractionType = json
  Fields = [
    """exa_json_path=$.source,exa_field_name=host"""
    """exa_json_path=$..timestamp,exa_field_name=time"""
    """exa_json_path=$..title,exa_field_name=alert_name"""
    """exa_json_path=$..signature,exa_field_name=alert_type"""
    """exa_json_path=$..severity,exa_field_name=alert_severity"""
    """exa_json_path=$..id,exa_field_name=alert_id"""
    """exa_json_path=$..description,exa_field_name=additional_info"""
    """exa_json_path=$..source.ip,exa_regex=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))"""
    """exa_regex="source":\{[^=]+?"host_name":"({src_host}[\w.-]+)""""
    """exa_json_path=$..source.port,exa_field_name=src_port"""
    """exa_json_path=$..source.mac,exa_field_name=src_mac"""
    """exa_json_path=$..source.country,exa_field_name=src_country"""
    """exa_json_path=$..source.inferred.os,exa_field_name=os"""
    """exa_json_path=$..destination.ip,exa_regex=({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))"""
    """exa_json_path=$..destination.port,exa_field_name=dest_port"""
    """exa_json_path=$..destination.mac,exa_field_name=dest_mac"""
    """exa_json_path=$..destination.country,exa_field_name=dest_country"""
  
}
```