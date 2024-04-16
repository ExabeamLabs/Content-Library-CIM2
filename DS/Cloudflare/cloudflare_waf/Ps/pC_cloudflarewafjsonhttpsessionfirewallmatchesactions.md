#### Parser Content
```Java
{
Name = cloudflare-waf-json-http-session-firewallmatchesactions
  Vendor = Cloudflare
  Product = Cloudflare WAF
  ExtractionType = json
  TimeFormat = "epoch"
  Conditions = [ """"WAFAction":"""", """ResponseStatus"""", """FirewallMatchesActions""", """"ZoneName":"""" ]
  Fields = [
    """exa_json_path=$.EdgeStartTimestamp,exa_regex=({time}\d{13})""",
    """exa_json_path=$.ClientDeviceType,exa_field_name=device_type""",
    """exa_json_path=$.ClientCountry,exa_field_name=src_country""",
    """exa_json_path=$.ClientIP,exa_regex=(?:["]+|({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?)""",
    """exa_json_path=$.ClientSrcPort,exa_field_name=src_port""",
    """exa_json_path=$.ClientRequestUserAgent,exa_field_name=user_agent""",
    """exa_json_path=$.ClientRequestBytes,exa_field_name=bytes_in""",
    """exa_json_path=$.EdgeResponseBytes,exa_field_name=bytes_out""",
    """exa_json_path=$.EdgeResponseStatus,exa_regex=({edge_response_status}({http_response_code}\d\d\d))"""
    """exa_json_path=$.OriginResponseStatus,exa_regex=({origin_response_status}({http_response_code}\d\d\d))"""
    """exa_json_path=$.EdgeServerIP,exa_regex=({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?""",
    """exa_json_path=$.OriginIP,exa_regex=({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?"*[^=]+?OriginResponseBytes":({bytes_out}\d+)""",
    """exa_json_path=$.OriginIP,exa_regex=(?:["]+|({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?)""",
    """exa_json_path=$.ClientRequestMethod,exa_field_name=method""",
    """exa_json_path=$.FirewallMatchesActions[0],exa_field_name=action""",
    """exa_regex="ClientRequestHost":"({web_domain}[^"]+?)(:\d+)?"""",
    """exa_regex="ClientRequestURI":"({uri_path}[^"\?\s]+)(?:\?({uri_query}[^?\s"]+))?""",
    """exa_json_path=$.ClientRequestProtocol,exa_field_name=protocol""",
    """exa_json_path=$.ClientRequestReferer,exa_field_name=referrer""",
    """exa_json_path=$.EdgeResponseContentType,exa_field_name=mime""",
    """exa_json_path=$.SecurityLevel,exa_field_name=alert_severity""",
    """exa_json_path=$.RayID,exa_field_name=alert_id""",
    """exa_json_path=$.WAFAction,exa_field_name=proxy_action,exa_match_expr=!InList(toLower($.WAFAction), "unknown")""",
    """exa_json_path=$.WAFRuleID,exa_field_name=event_code""",
    """exa_json_path=$.WAFRuleMessage,exa_field_name=additional_info"""
  ]
  ParserVersion = v1.0.0


}
```