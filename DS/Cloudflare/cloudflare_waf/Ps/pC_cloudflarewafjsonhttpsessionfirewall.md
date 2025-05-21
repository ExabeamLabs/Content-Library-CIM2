#### Parser Content
```Java
{
Name = cloudflare-waf-json-http-session-firewall
  ParserVersion = v1.0.0
  Vendor = Cloudflare
  Product = Cloudflare WAF
  ExtractionType = json
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Conditions = [  """ClientRequestUserAgent""", """"ClientIPClass":"""", """"ClientASN":""", """"ClientCountry":"""", """"ClientIP":"""", """"RayID":"""", """"EdgeColoCode":"""" ]
  Fields = [
    """"ClientRequestHost":"({host}[\w\-.]+)""",
    """"RayID":"({alert_id}[^"]+)""",
    """"ClientCountry":"({src_country}[^"]+)""",
    """"ClientIP":"(?:["]+|({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?)""",
    """"ClientSrcPort":({src_port}\d+)""",
    """"ClientRequestUserAgent":"({user_agent}[^"]+)""",
    """"EdgeResponseStatus":({edge_response_status}({http_response_code}\d\d\d))"""
    """"OriginResponseStatus":({origin_response_status}({http_response_code}\d\d\d))"""
    """"ClientRequestMethod":"(UNKNOWN|({method}[^"]+))""",
    """"ClientRequestHost":"({web_domain}[^"]+)""",
    """"ClientRequestProtocol":"({protocol}[^"]+)""",
    """"ClientDeviceType":"({device_type}[^"]+)"""",
    """"ClientRequestURI":"({uri}[^"]+)"""",
    """"ClientRequestBytes":({bytes}\d+)""",
    """exa_json_path=$.ClientRequestHost,exa_field_name=host""",
    """exa_json_path=$.RayID,exa_field_name=alert_id""",
    """exa_json_path=$.ClientCountry,exa_field_name=src_country""",
    """exa_json_path=$.ClientIP,exa_regex=(?:["]+|({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?)""",
    """exa_json_path=$.ClientSrcPort,exa_field_name=src_port""",
    """exa_json_path=$.ClientRequestUserAgent,exa_field_name=user_agent""",
    """exa_json_path=$.EdgeResponseStatus,exa_regex=({edge_response_status}({http_response_code}\d\d\d))"""
    """exa_json_path=$.OriginResponseStatus,exa_regex=({origin_response_status}({http_response_code}\d\d\d))"""
    """exa_json_path=$.ClientRequestMethod,exa_field_name=method,exa_match_expr=!InList(toLower($.ClientRequestMethod),"unknown")""",
    """exa_json_path=$.ClientRequestHost,exa_field_name=web_domain""",
    """exa_json_path=$.ClientRequestProtocol,exa_field_name=protocol""",
    """exa_json_path=$.ClientDeviceType,exa_field_name=device_type""",
    """exa_json_path=$.ClientRequestURI,exa_field_name=uri""",
    """exa_json_path=$.ClientRequestBytes,exa_field_name=bytes"""
    ]


}
```