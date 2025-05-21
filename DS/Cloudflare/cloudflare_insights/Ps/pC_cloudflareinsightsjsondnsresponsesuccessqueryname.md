#### Parser Content
```Java
{
Name = cloudflare-insights-json-dns-response-success-queryname
  Vendor = Cloudflare
  Product = Cloudflare Insights
  ParserVersion = "v1.0.0"
  ExtractionType = json
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ssZ"
  Conditions = [ """destinationServiceName =Cloudflare""", """"ColoCode":"""", """"QueryName":""" ]
  Fields = [
    """exa_json_path=$.Timestamp,exa_field_name=time"""
    """exa_json_path=$.SourceIP,exa_regex=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
    """exa_json_path=$.QueryType,exa_field_name=dns_query_type"""
    """exa_json_path=$.ResponseCode,exa_field_name=dns_response_code"""
    """exa_json_path=$.QueryName,exa_field_name=dns_query"""
    """exa_json_path=$.ColoCode,exa_field_name=additional_info""" 
  ]


}
```