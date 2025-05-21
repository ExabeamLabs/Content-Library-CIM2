#### Parser Content
```Java
{
Name = "pingidentity-pi-json-endpoint-app-activity-success"
  ParserVersion = "v1.0.0"
  Vendor = Ping Identity
  Product = Ping Identity
  ExtractionType = json
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSSSSZ"
  Conditions = [""""app":"ping-cloud"""", """"kubernetes":""", """"container_name"""", """"log_group":"application"""", """"stream":"stdout"""" ]
  Fields  = [
    """exa_json_path=$.@timestamp,exa_field_name=time"""
    """exa_json_path=$.host,exa_field_name=host"""
    """exa_json_path=$..container_image,exa_field_name=image_name"""
    """exa_json_path=$..role,exa_field_name=service_name"""
    """exa_json_path=$..app,exa_field_name=app"""
    """exa_json_path=$..pod_id,exa_field_name=instance_id"""
    """exa_regex=requesterIP=\\*"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))"""
    """exa_regex=resultCodeName =\\*"({result}[^"\\]+)\\*""""
  ]


}
```