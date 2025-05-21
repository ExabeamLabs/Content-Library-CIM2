#### Parser Content
```Java
{
Name = "crowdstrike-falcon-mix-endpoint-login-success-useridentity"
  ParserVersion = "v1.0.0"
  Vendor = "CrowdStrike"
  Product = "Falcon"
  TimeFormat = "epoch_sec"
  ExtractionType = json
  Conditions = [ 
"""event_simpleName":"""
""""UserIdentity""""
""""aid"""" 
]
  Fields = [
"""\"timestamp\":\s*\"({time}\d{10})"""
"""\"UserPrincipal\":\s*\"\s*(?:[^\"@]+@)?({domain}[^\"]+?)\s*""""
"""\"aid\":\s*\"({aid}[^\"]+)"""
"""\"event_simpleName\":\s*\"({event_code}[^\"]+)"""
"""\"LogonType\":\s*\"({login_type}\d+)"""
"""\"UserName\":\s*\"(({full_name}({first_name}[^\s\"]+)\s({last_name}[^\"]+)))"""
""""UserName":\s*"(({user_uid}[A-Fa-f0-9]+-[A-Fa-f0-9]+-[A-Fa-f0-9]+-[A-Fa-f0-9]+-[A-Fa-f0-9]+)|({user_sid}S-[^"]+)|({email_address}([A-Za-z0-9]+[!#$%&'+-\/=?^_`~])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)|({user}[\w\.\-\!\#\^\~]{1,40}\$?))""""
"""\"+AuthenticationPackage\"+:\s*\"+({auth_package}[^\"]+)\"+,"""
""""event_platform\\?":\\?"({os}[^"]+)\\?""""
""""aip":"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
""""cid":"({cid}[^"]+)"""
""""LogonDomain":"\s*({domain}[^\"]+?)\s*""""
"""exa_json_path=$.timestamp,exa_field_name=time""",
"""exa_regex="UserPrincipal\":\s*\"\s*(?:[^\"@]+@)?({domain}[^\"]+?)\s*""""
"""exa_json_path=$.event_simpleName,exa_field_name=event_code""",
"""exa_json_path=$.aid,exa_field_name=aid""",
"""exa_json_path=$.LogonType,exa_field_name=login_type""",
"""exa_regex="UserName\":\s*\"(({full_name}({first_name}[^\s\"]+)\s({last_name}[^\"]+)))"""
"""exa_regex="UserName":\s*"(({user_uid}[A-Fa-f0-9]+-[A-Fa-f0-9]+-[A-Fa-f0-9]+-[A-Fa-f0-9]+-[A-Fa-f0-9]+)|({user_sid}S-[^"]+)|({email_address}([A-Za-z0-9]+[!#$%&'+-\/=?^_`~])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)|({user}[\w\.\-\!\#\^\~]{1,40}\$?))""""
"""exa_json_path=$.AuthenticationPackage,exa_field_name=auth_package""",
"""exa_json_path=$.event_platform,exa_field_name=os""",
"""exa_regex="aip":"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
"""exa_json_path=$.cid,exa_field_name=cid""",
"""exa_json_path=$.LogonDomain,exa_field_name=domain""",
  ]


}
```