#### Parser Content
```Java
{
Name = envoy-e-json-http-session-http
  Vendor = Envoy
  Product = Envoy
  ParserVersion = v1.0.0
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  ExtractionType = json
  Conditions = [""""request":""",""""response":""",""""downstreamLocalAddress":""",""""downstreamDirectRemoteAddress":"""]
  Fields = [
    """exa_json_path=$..user,exa_field_name=user"""
    """exa_json_path=$.request.requestMethod,exa_field_name=method"""
    """exa_json_path=$.request.requestBodyBytes,exa_field_name=bytes_in"""
    """exa_json_path=$.response.responseBodyBytes,exa_field_name=bytes_out"""
    """exa_json_path=$.response.responseCode,exa_field_name=http_response_code"""
    """exa_json_path=$.protocolVersion,exa_field_name=protocol"""
    """exa_json_path=$.request.userAgent,exa_field_name=user_agent"""
    """exa_json_path=$..downstreamLocalAddress..address,exa_regex=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
    """exa_json_path=$..downstreamLocalAddress..portValue,exa_field_name=src_port"""
    """exa_json_path=$..upstreamRemoteAddress..portValue,exa_field_name=dest_port"""
    """exa_json_path=$..upstreamRemoteAddress..address,exa_regex=({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?"""
    """exa_json_path=$.response.responseCodeDetails,exa_field_name=additional_info"""
  ]


}
```