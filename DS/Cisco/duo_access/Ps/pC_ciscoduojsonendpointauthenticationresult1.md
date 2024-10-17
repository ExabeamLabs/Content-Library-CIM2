#### Parser Content
```Java
{
Name = cisco-duo-json-endpoint-authentication-result-1
  Vendor = Cisco
  Product = Duo Access
  ExtractionType = json
  TimeFormat = "epoch_sec"
  ParserVersion = "v1.0.0"
  Conditions = [ """"event_type":"""", """"result":""", """"user":""", """"access_device":""", """"timestamp":""" ]
  Fields = [
    """"timestamp":({time}\d{10})""",
    """"host":"+({host}[\w\-\.]+)"""",
    """"ip":"+(0.0.0.0|null|({src_ip}[a-fA-F:\.\d]+))"""",
    """"result":"({action}[^"]+)"""",
    """"reason":"({failure_reason}[^"]+)"[^=]+?"result":"(denied|fraud|failure|error)"""",
    """"result":"(denied|fraud|failure|error)"[^=]+?"reason":"({failure_reason}[^"]+)"""",
    """"os":"({os}[^"]+)"""",
    """"os_version":"({os_version}[^"]+)"""",
    """"browser":"(Unknown|({browser}[^"]+))"""",
    """"browser_version":"({browser_version}[^"]+)"""",
    """"email":"({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))"""",
    """"factor":"(?:n\/a|({factor}[^"]+))"""",
    """"user":[^\}]+?"name":"({user}[\w\.\-\!\#\^\~]{1,40}\$?)""""
    """"application".+?"name":\s*"({service_name}[^"]+)"""
    """"access_device":\{.*?"location":\{[^\}]*?"country":"(null|({src_country}[^"]+))"""",
    """"access_device":\{.*?"location":\{[^\}]*?"country":"(null|({mfa_country}[^"]+))"""",
    """"auth_device":\{.*?"location":\{[^\}]*?"country":"(null|({mfa_country}[^"]+))"""",
    """"access_device":.+?"hostname":"({mfa_device}[^"]+)""",
    """exa_json_path=$.timestamp,exa_regex=({time}\d{10})""",
    """exa_json_path=$.host,exa_field_name=host""",
    """exa_json_path=$.access_device.ip,exa_regex=(0.0.0.0|null|({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4})))(:({src_port}\d+))?""",
    """exa_json_path=$.result,exa_field_name=action""",
    """exa_regex="reason":"({failure_reason}[^"]+)"[^=]+?"result":"(denied|fraud|failure|error)"""",
    """exa_regex="result":"(denied|fraud|failure|error)"[^=]+?"reason":"({failure_reason}[^"]+)"""",
    """exa_json_path=$.access_device.os,exa_field_name=os""",
    """exa_json_path=$.access_device.os_version,exa_field_name=os_version""",
    """exa_json_path=$.access_device.browser,exa_field_name=browser""",
    """exa_json_path=$.email,exa_regex=({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))""",
    """exa_json_path=$.factor,exa_field_name=factor,exa_match_expr=!Contains($.factor,"n/a")""",
    """exa_json_path=$.user.name,exa_regex=({user}[\w\.\-\!\#\^\~]{1,40}\$?)""",
    """exa_json_path=$.application.name,exa_field_name=service_name""",
    """exa_json_path=$.access_device.location.country,exa_field_name=src_country""",
    """exa_json_path=$.access_device.location.country,exa_field_name=mfa_country""",
    """exa_json_path=$.auth_device.location.country,exa_field_name=mfa_country,exa_match_expr=!Contains($.auth_device.location.country,"null")""",
    """exa_json_path=$.access_device.hostname,exa_field_name=mfa_device,exa_match_expr=!Contains($.access_device.hostname,"null")"""
  ]


}
```