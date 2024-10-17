#### Parser Content
```Java
{
Name = crowdstrike-falcon-json-endpoint-logout-success-userlogoff
  Vendor = CrowdStrike
  Product = Falcon
  ExtractionType = json
  ParserVersion = "v1.0.0"
  TimeFormat = ["epoch_sec","epoch"]
  Conditions = [ """"event_simpleName":"UserLogoff"""", """"LogonType":""" ]
  Fields = [
    """timestamp":"({time}\d{10,13})""",
    """"event_simpleName":"({event_name}[^"]+)"""",
    """"UserName":\s*"(({user_uid}[A-Fa-f0-9]+-[A-Fa-f0-9]+-[A-Fa-f0-9]+-[A-Fa-f0-9]+-[A-Fa-f0-9]+)|({linked_service_account}OVService[^"]+)|({user_sid}S-[^"]+)|({user}[\w\.\-\!\#\^\~]{1,40}\$?))""""
    """"LogonType":"({login_type}\d+)"""
    """"aip":\s*"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))"""",
    """"aid":"({aid}[^"]+)"""",
    """"LogonDomain":"({domain}[^"]+)"""",
    """"AuthenticationPackage":"({auth_package}[^"]+)"""",
    """"UserSid":"({user_sid}[^"]+)""",
    """"UserPrincipal":"({email_address}([A-Za-z0-9]+[!#$%&'+-\/=?^_`~])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)(?<!(local))(?<!(loc))(?<!(localdomain))"""",
    """"event_platform":"({os}[^"]+)"""",
    """exa_json_path=$.timestamp,exa_field_name=time""",
    """exa_json_path=$.event_simpleName,exa_field_name=event_name""",
    """exa_json_path=$.UserName,exa_regex=(({user_uid}[A-Fa-f0-9]+-[A-Fa-f0-9]+-[A-Fa-f0-9]+-[A-Fa-f0-9]+-[A-Fa-f0-9]+)|({linked_service_account}OVService[^"]+)|({user_sid}S-[^"]+)|({user}[\w\.\-\!\#\^\~]{1,40}\$?))""",
    """exa_json_path=$.LogonType,exa_field_name=login_type""",
    """exa_json_path=$.aip,exa_regex=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))""",
    """exa_json_path=$.aid,exa_field_name=aid""",
    """exa_json_path=$.LogonDomain,exa_field_name=domain""",
    """exa_json_path=$.AuthenticationPackage,exa_field_name=auth_package""",
    """exa_json_path=$.UserSid,exa_field_name=user_sid""",
    """exa_json_path=$.UserPrincipal,exa_regex=({email_address}([A-Za-z0-9]+[!#$%&'+-\/=?^_`~])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)(?<!(local))(?<!(loc))(?<!(localdomain))""",
    """exa_regex="UserPrincipal":"({email_address}([A-Za-z0-9]+[!#$%&'+-\/=?^_`~])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)(?<!(local))(?<!(loc))(?<!(localdomain))"""",
    """exa_json_path=$.event_platform,exa_field_name=os"""
  ]


}
```