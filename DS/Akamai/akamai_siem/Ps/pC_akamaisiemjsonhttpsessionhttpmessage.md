#### Parser Content
```Java
{
Name = akamai-siem-json-http-session-httpmessage
   Vendor = Akamai 
   Product = Akamai SIEM
   ExtractionType = json
   TimeFormat = "epoch_sec"
   Conditions = [ """"httpMessage":""", """"type":"akamai_siem"""", """"attackData":""" ]
   Fields = [
    """exa_json_path=$..clientIP,exa_regex=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
    """exa_json_path=$.httpMessage.start,exa_field_name=time""",
    """exa_json_path=$.httpMessage.protocol,exa_field_name=protocol""",
    """exa_json_path=$.httpMessage.method,exa_field_name=method""",
    """exa_json_path=$.httpMessage.host,exa_field_name=web_domain""",
    """exa_json_path=$.httpMessage.port,exa_field_name=dest_port""",
    """exa_json_path=$.httpMessage.path,exa_field_name=uri_path""",
    """exa_json_path=$.httpMessage.status,exa_field_name=http_response_code""",
    """exa_json_path=$.httpMessage.bytes,exa_field_name=bytes""",
    """exa_json_path=$.attackData.policyId,exa_field_name=policy_id""",
    """exa_json_path=$.updatedhttpMessage.requestHeaders.User-Agent,exa_regex=\s*({user_agent}[^"$]+)""",
    """exa_json_path=$.identity,exa_field_name=identities"""
   ]
   ParserVersion = v1.0.0


}
```