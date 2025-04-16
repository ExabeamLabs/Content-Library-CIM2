#### Parser Content
```Java
{
Name = cisco-duo-json-endpoint-authentication-ip
  Vendor = Cisco
  Product = "Cisco Identity and Access Management"
  ExtractionType = json
  TimeFormat = "epoch_sec"
  Conditions = [ """"new_enrollment"""",""""ip"""",""""result""""]
  Fields = [
    """exa_json_path=$.host,exa_field_name=host""",
    """exa_json_path=$.timestamp,exa_regex=({time}\d{10})""",
    """exa_json_path=$.device,exa_field_name=device_name,exa_match_expr=!InList(toLower($.device),"null")""",
    """exa_json_path=$.ip,exa_regex=(0.0.0.0|({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?)""",
    """exa_regex="username"\s*:\s*"(?:({domain}[^\\"]+)\\+)?({user}[\w\.\-\!\#\^\~]{1,40}\$?)""",
    """exa_json_path=$.factor,exa_field_name=factor,exa_match_expr=!InList(($.factor), "n/a")""",
    """exa_json_path=$.os,exa_field_name=os""",
    """exa_json_path=$.os_version,exa_field_name=os_version""",
    """exa_json_path=$.browser,exa_field_name=browser""",
    """exa_json_path=$.browser_version,exa_field_name=browser_version""",
    """exa_json_path=$.result,exa_field_name=action""",
    """exa_json_path=$.reason,exa_field_name=failure_reason""",
    """exa_json_path=$.new_enrollment,exa_field_name=new_enrollment""",
    """exa_json_path=$.integration,exa_field_name=service_name""",
    """exa_json_path=$.email,exa_regex=({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))""",
    """exa_json_path=$.location.country,exa_field_name=mfa_country"""
  ]
  DupFields = ["device_name->mfa_device"]
  ParserVersion = "v1.0.0"


}
```