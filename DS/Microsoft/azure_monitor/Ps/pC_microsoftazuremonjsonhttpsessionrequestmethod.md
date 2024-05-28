#### Parser Content
```Java
{
Name = microsoft-azuremon-json-http-session-requestmethod
  Vendor = Microsoft
  Product = Azure Monitor
  ParserVersion = "v1.0.0"
  ExtractionType = json
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSSSSSZ"
  Conditions = [ """"RequestMethod":"""", """"ResponseStatusCode":""", """"UserAgent":"""", """"RequestUri":"""", """"_ItemId":""""]
  Fields = [
    """exa_json_path=$.TimeGenerated,exa_field_name=time""",
    """exa_json_path=$.Location,exa_field_name=region""",
    """exa_json_path=$.UserAgent,exa_field_name=user_agent""",
    """exa_json_path=$.RequestMethod,exa_field_name=method""",
    """exa_json_path=$.RequestUri,exa_regex=({url}(({protocol}(\w+)?):\/\/)?({web_domain}[^"\/\s]+)({uri_path}\/[^\?"\s]*)?({uri_query}\?[^"\s]*)?)""",
    """exa_json_path=$.UserId,exa_field_name=user_id""",
    """exa_json_path=$.Location,exa_field_name=region""",
    """exa_json_path=$.RequestSizeBytes,exa_field_name=bytes_in""",
    """exa_json_path=$.ResponseSizeBytes,exa_field_name=bytes_out""",
    """exa_json_path=$.ResponseStatusCode,exa_field_name=http_response_code"""
  ]


}
```