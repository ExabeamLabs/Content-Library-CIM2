#### Parser Content
```Java
{
Name = infoblox-bddi-json-http-request-success-nginx_access
    Vendor = Infoblox
    Product = BloxOne DDI
    ExtractionType = json
    TimeFormat = "yyyy-MM-dd'T'HH:mm:ssZ"
    Conditions = [ """"fluentd_time"""", """"http_user_agent"""", """"remote_addr"""", """"nginx.access"""" ]
    Fields = [
      """exa_json_path=$.host,exa_field_name=host"""
      """exa_json_path=$.http_user_agent,exa_field_name=user_agent"""
      """exa_json_path=$.security_event_type,exa_field_name=event_name"""
      """exa_json_path=$.timestamp,exa_field_name=time"""
      """exa_json_path=$.app,exa_field_name=app"""
      """exa_json_path=$.remote_addr,exa_field_name=dest_ip"""
      """exa_json_path=$.jwt.username,exa_field_name=user"""
      """exa_json_path=$.status,exa_field_name=http_response_code"""
      """exa_json_path=$.x-geo-country-name,exa_field_name=country"""
      """exa_json_path=$.request,exa_regex=({method}\w+)\s*({url}({uri_path}[^"]+?)(({uri_query}\?[^\s"]+)))\s({protocol}[^"\/]+)"""
    ]
    ParserVersion = "v1.0.0"

  

}
```