#### Parser Content
```Java
{
Name = "kong-kg-json-http-session-accesslog"
  Vendor = "Kong"
  Product = "Kong Gateway"
  ExtractionType = json
  ParserVersion = "v1.0.0"
  TimeFormat = "epoch_sec"
  Conditions = [ """"kong"""", """"request":{"""", """"response":{"""", """"route":{"""", """"service":{"""" ]
  Fields = [
    """exa_json_path=$.started_at,exa_field_name=time""",
    """exa_json_path=$.client_ip,exa_regex=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
    """exa_json_path=$.request.method,exa_field_name=method""",
    """exa_json_path=$.request.url,exa_regex=({url}(({protocol}https?)://)?({web_domain}[^"\/\s:]+)(:({dest_port}\d+))?({uri_path}\/[^\?"\s]*)?({uri_query}\?[^"\s]*)?)""",
    """exa_json_path=$.request.headers['user-agent'],exa_field_name=user_agent""",
    """exa_json_path=$.response.status,exa_field_name=http_response_code""",
    """exa_json_path=$.request.size,exa_field_name=bytes_in""",
    """exa_json_path=$.response.size,exa_field_name=bytes_out""",
    """exa_json_path=$.service.host,exa_field_name=dest_host""",
    """exa_json_path=$.service.port,exa_field_name=dest_port""",
    """exa_json_path=$.route.name,exa_field_name=service_name""",
    """exa_json_path=$.request.headers.operation,exa_field_name=operation""",
    """exa_json_path=$.request.headers['end-user-id'],exa_field_name=user_id""",
    """exa_json_path=$.request.headers['client-header'],exa_regex=({email_address}([A-Za-z0-9]+[!#$%&'+-\/=?^_`~])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,\|>]+))""",
    """exa_json_path=$.authenticated_entity.id,exa_field_name=account_id""",
    """exa_json_path=$.request.id,exa_field_name=event_id""",
    """exa_json_path=$.request.tls.cipher,exa_field_name=cipher"""
  ]


}
```