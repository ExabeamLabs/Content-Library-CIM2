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
       """exa_json_path=$.x-client-ip,exa_regex=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
       """exa_json_path=$.dst,exa_regex=({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?""",
       """exa_json_path=$.user-agent,exa_field_name=user_agent""",
       """exa_json_path=$.categories,exa_field_name=category""",
       """exa_json_path=$.userid,exa_regex=(({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))|({user}[\w\.\-\!\#\^\~]{1,40}\$?))""",
       """exa_json_path=$.url,exa_field_name=url""",
       """exa_json_path=$.protocol,exa_field_name=protocol""",
       """exa_json_path=$.referer,exa_field_name=referrer"""
        """exa_json_path=$.browser_and_version,exa_field_name=browser""",
        """exa_json_path=$.connId,exa_field_name=connection_id""",
        """exa_json_path=$.content-type,exa_field_name=mime""",
        """exa_json_path=$.domain,exa_field_name=domain""",
        """exa_json_path=$.origin_country,exa_field_name=src_country""",
        """exa_json_path=$.egress_ip,exa_field_name=host_ip""",
        """exa_json_path=$.origin_ip,exa_field_name=origin_ip""",
        """exa_json_path=$.pe_reason,exa_field_name=rule_reason""",
        """exa_json_path=$.pe_rulename,exa_field_name=rule""",
        """exa_json_path=$.region,exa_field_name=region""",
        """exa_json_path=$.request_type,exa_field_name=method""",
        """exa_json_path=$.response_code,exa_field_name=http_response_code""",
        """exa_json_path=$.risk_score,exa_field_name=severity""",
        """exa_regex=username="*({user}[\w\.\-\!\#\^\~]{1,40}\$?)""""
    ]
  

}
```