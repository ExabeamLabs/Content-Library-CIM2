#### Parser Content
```Java
{
Name = google-cloudplatform-json-app-activity-success-catchall_category
  TimeFormat = """yyyy-MM-dd'T'HH:mm:ss.SSSZ"""
  ParserVersion = "v1.0.0"
  Vendor = Google
  Product = Google Cloud Platform
  ExtractionType = json
  Conditions = [ """destinationServiceName =Google Cloud""", """dproc=Cloud PubSub""", """"category":""" ]
  Fields = [
    """exa_json_path=$.event.remote_address,exa_regex=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
    """exa_json_path=$.event.category,exa_field_name=category"""
    """exa_json_path=$.event.timestamp,exa_field_name=time"""
    """exa_json_path=$.event.username,exa_regex=({email_address}([A-Za-z0-9]+[!#$%&'+-\/=?^_~])*[A-Za-z0-9]+@[^\]\s"\\,\|]+.[^\]\s"\\,\|]+)"""
  ]


}
```