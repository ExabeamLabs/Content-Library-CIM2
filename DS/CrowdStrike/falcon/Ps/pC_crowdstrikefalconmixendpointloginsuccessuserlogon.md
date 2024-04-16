#### Parser Content
```Java
{
Name = "crowdstrike-falcon-mix-endpoint-login-success-userlogon"
  ParserVersion = "v1.0.0"
  Vendor = "CrowdStrike"
  Product = "Falcon"
  TimeFormat = "epoch_sec"
  ExtractionType = json
  Conditions = [ 
""""event_simpleName":"UserLogon""""
""""aid"""" 
]
  Fields = [
""""aip":"({aip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
"""suser=((?i)system|({user}[\w\.\-]{1,40}\$?))""",
"""suid=({user_sid}[^\s]+)""",
""""AuthenticationPackage":"({auth_package}[^\"]+)""",
""""timestamp":\s*"({time}\d{10})""",
""""LogonType":"({login_type}\d+)""",
""""UserPrincipal":"(({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+))(?<!LOCAL)(?<!local)(?<!loc)(?<!prd)(?<!localdomain)|({user}[\w\.\-]{1,40}\$?)(?:@({domain}[^,"]+)[^"]*)?)"""",
"""UserName":"((?i)system|({full_name}({first_name}[^\s"]+)\s({last_name}[^"]+))|(({email_address}([A-Za-z0-9]+[!#$%&'+-\/=?^_`~])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,\|]+))(?i))(?<!local)(?<!loc)|((\w+?_)?(\w+-)?\w+-\w+-\w+-\w+|({user}[\w\.\-]{1,40}\$?)(?:@({domain}[^"]+)[^"]*)?))"""",
""""UserName":\s*"(({user_uid}[A-Fa-f0-9]+-[A-Fa-f0-9]+-[A-Fa-f0-9]+-[A-Fa-f0-9]+-[A-Fa-f0-9]+)|({user_sid}S-[^"]+)|({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+))(?<!local)(?<!loc)|({user}[\w\.\-]{1,40}\$?)(?:@({domain}[^"]+)[^"]*)?)""""
""""LogonServer":"({auth_server}[^\"]+)""",
""""ClientComputerName"+:"+(-|({dest_host}[^\"\\,]+))""",
""""UserSid":"({user_sid}[^\"]+)""",
""""aid":"({aid}[^\"]+)""",
""""event_simpleName":"({event_code}[^\"]+)""",
""""LogonDomain":"(NT AUTHORITY|({domain}[^\"]+))""",
""""RemoteAddressIP4":"({dest_ip}[A-Fa-f:\d\.]+)"""",
""""event_platform":"({os}[^"\\]+)"""
""""aip":"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
""""cid":"({cid}[^"]+)"""
"""exa_json_path=$.aip,exa_field_name=aip"""
"""exa_regex="suser=((?i)system|({user}[\w\.\-]{1,40}\$?))"""
"""exa_regex="suid=({user_sid}[^\s]+)"""
"""exa_json_path=$.AuthenticationPackage,exa_field_name=auth_package"""
"""exa_json_path=$.timestamp,exa_field_name=time"""
"""exa_json_path=$.LogonType,exa_field_name=login_type"""
"""exa_regex="UserPrincipal":"(({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+))(?<!LOCAL)(?<!local)(?<!loc)(?<!prd)(?<!localdomain)|({user}[\w\.\-]{1,40}\$?)(?:@({domain}[^,"]+)[^"]*)?)"""",
"""exa_regex=UserName":"((?i)system|({full_name}({first_name}[^\s"]+)\s({last_name}[^"]+))|(({email_address}([A-Za-z0-9]+[!#$%&'+-\/=?^_`~])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,\|]+))(?i))(?<!local)(?<!loc)|((\w+?_)?(\w+-)?\w+-\w+-\w+-\w+|({user}[\w\.\-]{1,40}\$?)(?:@({domain}[^"]+)[^"]*)?))"""",
"""exa_regex=UserName":\s*"(({user_uid}[A-Fa-f0-9]+-[A-Fa-f0-9]+-[A-Fa-f0-9]+-[A-Fa-f0-9]+-[A-Fa-f0-9]+)|({user_sid}S-[^"]+)|({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+))(?<!local)(?<!loc)|({user}[\w\.\-]{1,40}\$?)(?:@({domain}[^"]+)[^"]*)?)""""
"""exa_json_path=$.LogonServer,exa_field_name=auth_server"""
"""exa_json_path=$.ClientComputerName,exa_field_name=dest_host,exa_match_expr=!InList($.ClientComputerName,"-")""",
"""exa_json_path=$.UserSid,exa_field_name=user_sid"""
"""exa_json_path=$.aid,exa_field_name=aid"""
"""exa_json_path=$.event_simpleName,exa_field_name=event_code"""
"""exa_json_path=$.LogonDomain,exa_field_name=domain,exa_match_expr=!InList($.LogonDomain,"NT AUTHORITY")""",
"""exa_json_path=$.RemoteAddressIP4,exa_regex=({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?"""
"""exa_json_path=$.event_platform,exa_field_name=os"""
"""exa_json_path=$.aip,exa_regex=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
"""exa_json_path=$.cid,exa_field_name=cid"""
  ]
  DupFields = [ "user->account", "aip->src_ip" ]


}
```