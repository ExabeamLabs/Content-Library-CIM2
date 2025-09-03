#### Parser Content
```Java
{
Name = illumio-ic-json-endpoint-authentication-fail-requestauthentication_failed
  ParserVersion = v1.0.0
  Vendor = Illumio
  Product = Illumio Core
  ExtractionType = json
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
  Conditions = [ """.illum.io""", """"info":{""", """"event_type":"""", """"request.authentication_failed"""" ]
  Fields = [
    """exa_json_path=$.severity,exa_field_name=alert_severity"""
    """exa_json_path=$.pce_fqdn,exa_field_name=web_domain"""
    """exa_json_path=$.timestamp,exa_field_name=time"""
    """exa_json_path=$.info.src_ip,exa_regex=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
    """exa_json_path=$.event_type,exa_field_name=event_name"""
    """exa_json_path=$.href,exa_field_name=uri_path"""
    """exa_json_path=$.notifications.uuid,exa_field_name=user_uid"""
    """exa_json_path=$.info.api_endpoint,exa_field_name=url"""
    """exa_json_path=$.info.api_method,exa_field_name=method"""
    """exa_json_path=$.status,exa_field_name=method"""    
  ]


}
```