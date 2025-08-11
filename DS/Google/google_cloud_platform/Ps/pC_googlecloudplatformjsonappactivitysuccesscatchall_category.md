#### Parser Content
```Java
{
Name = google-cloudplatform-json-app-activity-success-catchall_category
  TimeFormat = ["yyyy-MM-dd'T'HH:mm:ss.SSSZ","yyyy-MM-dd'T'HH:mm:ss.SSSSSSSSSZ","yyyy-MM-dd'T'HH:mm:ss.SSSSSSZ" ]
  ParserVersion = "v1.0.0"
  Vendor = Google
  Product = Google Cloud Platform
  ExtractionType = json
  Conditions = [ """destinationServiceName =Google Cloud""", """dproc=Cloud PubSub""", """"category":""" ]
  Fields = [
    """exa_json_path=$..remote_address,exa_regex=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
    """exa_json_path=$..category,exa_field_name=category"""
    """exa_json_path=$..timestamp,exa_field_name=time"""
    """exa_json_path=$..username,exa_regex=({email_address}([A-Za-z0-9]+[!#$%&'+-\/=?^_~])*[A-Za-z0-9]+@[^\]\s"\\,\|]+.[^\]\s"\\,\|]+)"""
    """exa_json_path=$..eventTime,exa_field_name=time"""
    """exa_json_path=$..service,exa_field_name=service_name"""
    """exa_json_path=$..cloudProvider,exa_field_name=provider_name"""
    """exa_json_path=$..location,exa_field_name=region""",
    """exa_json_path=$.resource.type,exa_field_name=resource_type""",
    """exa_json_path=$..severity,exa_field_name=severity"""
     """exa_json_path=$..resourceName,exa_regex=({resource_path}({resource_dir}[^"]+)\/({resource_name}[^"\/]+))""",
  ]


}
```