#### Parser Content
```Java
{
Name = menlo-ms-json-http-session-security
    Vendor = Menlo Security
    Product = Menlo Security
    TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSSSS"
    ExtractionType = json
    ParserVersion = "v1.0.0"
    Conditions = [ """"Menlo Security"""", """"browser_and_version":""", """"request_type":""", """"connId":""", """"userid":""", """"content-type":""", """"user-agent":""" ]
    Fields = [
       """exa_json_path=$.event_time,exa_field_name=time""",
       """exa_json_path=$.pe_action,exa_field_name=action""",
       """exa_json_path=$.host,exa_field_name=host""",
       """exa_json_path=$.x-client-ip,exa_field_name=src_ip""",
       """exa_json_path=$.dst,exa_field_name=dest_ip""",
       """exa_json_path=$.user-agent,exa_field_name=user_agent""",
       """exa_json_path=$.categories,exa_field_name=category""",
       """exa_json_path=$.userid,exa_regex=(({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))|({user}[\w\.\-]{1,40}\$?))""",
       """exa_json_path=$.url,exa_field_name=url""",
       """exa_json_path=$.protocol,exa_field_name=protocol""",
       """exa_json_path=$.referer,exa_field_name=referrer"""
    ]
  

}
```