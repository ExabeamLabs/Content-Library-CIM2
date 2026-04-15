#### Parser Content
```Java
{
Name = barracuda-waf-str-http-request-success-defaultunprotectedvalid
  ParserVersion = v1.0.0
  Conditions = [ """INTERNAL""", """DEFAULT""", """UNPROTECTED""" ]

barracuda-web-activity}{
  Name = barracuda-waf-str-http-request-success-profiledvalid
  ParserVersion = v1.0.0
  Conditions = [ """SERVER""", """PROFILED""", """PROTECTED""", """VALID""" barracuda-web-activity = {
  Vendor = Barracuda
  Product = Barracuda WAF
  TimeFormat =  [ "yyyy-MM-dd HH:mm:ss.SSS Z", "epoch" ]
  ExtractionType = json
  Fields = [
    """({time}\d\d\d\d-\d\d-\d\d \d\d:\d\d:\d\d\.\d+ (\+|\-)\d+)\s+(?:-|({host}\S+))\s+(\S+\s+){2}(?:-|({dest_port}\d+))\s+(?:-|({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?)\s+(?:-|({=src_port}\d+))\s+(\S+\s+){2}(?:-|({method}(GET|POST)))\s+(?:-|({protocol}\S+))\s+(?:-|\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3}|({web_domain}\S+))\s+\S+\s+(?:-|({http_response_code}\d+))\s+(?:-|({bytes_out}\d+))\s+(?:-|({bytes_in}\d+))\s+(\S+\s+){2}(?:-|({dest_translated_ip}\S+))\s+(?:-|({=dest_port}\d+))\s+(\S+\s+){5}(?:-|({action}\S+))\s+(?:-|({uri_path}\S+))\s+(?:"-"|({uri_query}[^"]+?))\s+(?:"-"|({url}[\w\-]+:\/\/\S+))\s+(?:"-"|([^"]*?))\s+"(?:-|({user_agent}[^"]+))"\s+(\S+\s+){2}(?:"-"|({user}[\w\.\-\!\#\^\~]{1,40}\$?))""",#dl field removed
    """(POST|GET)\s+\S+\s+({web_domain}[^\s]*(?:\.(?:com|net|info|edu|org|gov|co|jp|ru|de|ir|it|in|fr|info|pl|nl|es|gr|cz|eu|tv|me|jp|ca|cn|uk|my|cc|id|us|nz|biz|club|io|gg|fi|au|st|tw|asia|sg|ie|li|za|ch))+)\s"""
    """Mozilla\/[^"]+\(({os}iOS|Android|BlackBerry|Windows Phone|BeOS|(?:X|x)11|(?:W|w)indows|(?:L|l)inux|(?:M|m)acintosh|(?:D|d)arwin|iPhone)[^"]+?({browser}Chrome|Safari|Opera|(?:F|f)irefox|MSIE|Trident)""",
    """exa_json_path=$.UniqueID,exa_field_name=transaction_id""",
    """exa_json_path=$.LoginID,exa_field_name=login_id""",
    """exa_json_path=$.DC_ID,exa_field_name=domain_controller""",
    """exa_json_path=$.ClientPort,exa_field_name=src_port""",
    """exa_json_path=$.Version,exa_field_name=version""",
    """exa_json_path=$.RuleName,exa_field_name=rule""",
    """exa_json_path=$.ProfileMatched,exa_field_name=profile""",
    """exa_json_path=$.ServiceIP,exa_field_name=dest_ip""",
    """exa_json_path=$.Method,exa_field_name=method""",
    """exa_json_path=$.ClientIP,exa_field_name=src_ip""",
    """exa_json_path=$.ResponseType,exa_field_name=response_type""",
    """exa_json_path=$.BytesSent,exa_field_name=bytes_out""",
    """exa_json_path=$.BytesReceived,exa_field_name=bytes_in""",
    """exa_json_path=$.ProxyIP,exa_field_name=proxy_ip""",
    """exa_json_path=$.HTTPStatus,exa_field_name=http_response_code""",
    """exa_json_path=$.ServicePort,exa_field_name=dest_port""",
    """exa_json_path=$.ClientType,exa_field_name=client_type""",
    """exa_json_path=$.EpochTime,exa_field_name=time""",
    """exa_json_path=$.AuthenticatedUser,exa_regex=(-|({user}[\w\.\-\!\#\^\~]{1,40}\$?))""",
    """exa_json_path=$.URL,exa_field_name=url""",
    """exa_json_path=$.UserAgent,exa_field_name=user_agent""",
    """exa_json_path=$.Protocol,exa_field_name=protocol""",
    """exa_json_path=$.ClientIP_country_code,exa_field_name=country_code""",
    """exa_json_path=$.destinationServiceName,exa_field_name=app""",
    """exa_json_path=$.Referer,exa_field_name=referrer""",
    """exa_json_path=$.Host,exa_field_name=host"""
  ]
}
}
```