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
    """exa_json_path=$..start,exa_field_name=time""",
    """exa_json_path=$..protocol,exa_field_name=protocol""",
    """exa_json_path=$..method,exa_field_name=method""",
    """exa_json_path=$..host,exa_field_name=web_domain""",
    """exa_json_path=$..port,exa_field_name=dest_port""",
    """exa_json_path=$..path,exa_field_name=uri_path""",
    """exa_json_path=$..status,exa_field_name=http_response_code""",
    """exa_json_path=$..bytes,exa_field_name=bytes""",
    """exa_json_path=$..policyId,exa_field_name=policy_id"""
   ]
   ParserVersion = v1.0.0


}
```