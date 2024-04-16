#### Parser Content
```Java
{
Name = kasada-k-json-http-session-nonstatic
  ExtractionType = json
  Vendor = Kasada
  Product = Kasada
  ParserVersion = "v1.0.0"
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
  Conditions = [ """"logType":"HTTP-Transaction"""",""""clientResCode"""",""""access-control-expose-headers"""",""""resourceType":"NON_STATIC_RESOURCE"""" ]
  Fields = [
    """exa_json_path=$.logType,exa_field_name=event_category""",
    """exa_json_path=$.timestamp,exa_field_name=time""",
    """exa_json_path=$.reason,exa_field_name=proxy_action""",
    """exa_json_path=$.clientResCode,exa_field_name=http_response_code""",
    """exa_json_path=$.clientTokenID,exa_field_name=client_token""",
    """exa_json_path=$.action,exa_field_name=action""",
    """exa_json_path=$.method,exa_field_name=method""",
    """exa_json_path=$.level,exa_field_name=alert_severity""",
    """exa_json_path=$.ip,exa_regex=(?:|({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?)$""",
    """exa_json_path=$.url,exa_field_name=url""",
    """exa_json_path=$.reqHeaders.host,exa_field_name=host""",
    """exa_json_path=$.reqHeaders.content-type,exa_field_name=mime""",
    """exa_json_path=$.reqHeaders.x-amplitude-session-id,exa_field_name=session_id""",
    """exa_json_path=$.reqHeaders.user-agent,exa_field_name=user_agent""",
    """exa_json_path=$.domain,exa_field_name=domain""",
    """exa_json_path=$.resHeaders.server,exa_field_name=server""",
    """exa_json_path=$.resourceType,exa_field_name=resource_type""",
	]


}
```