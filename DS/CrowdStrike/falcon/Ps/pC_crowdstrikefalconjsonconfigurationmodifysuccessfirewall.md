#### Parser Content
```Java
{
Name = "crowdstrike-falcon-json-configuration-modify-success-firewall"
  Vendor = "CrowdStrike"
  Product = "Falcon"
  ExtractionType = json
  TimeFormat = "epoch_sec"
  Conditions = [
    """"event_simpleName":"Firewall"""
  ]
  Fields = [
    """\"hostname\":\"({host}[\w\-.]+)\""""
    """\"timestamp\":\"({time}\d{10})"""
    """\"event_simpleName\":\"({event_code}({operation}[^\"]+))"""
    """\"aid\":\"({aid}[^\"]+)"""
    """\"FirewallRule\":\"({additional_info}[^\"]+)"""
    """\"UserName\":\"(({email_address}[^@\"]+@[^\"]+)|({user}[\w\.\-\!\#\^\~]{1,40}\$?))\""""
    """src-account-name\":\"({account_name}[^\"]+)"""
    """"FirewallOption":"({action}[^"]+)""""
    """"FirewallRuleId":"({rule_id}[^"\s]+)""""
    """"FirewallRule":"({rule}[^"]+)","""
    """"event_platform":"({os}[^"]+)""""
    """"cid":"({cid}[^"]+)"""
    """"LocalAddressIP4":"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""""
    """"ComputerName":"({host}[\w\-\.]+)""""
    """"aip":\s*"({aip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""""
    """exa_regex="hostname":"({host}[\w\-.]+)"""",
    """exa_json_path=$.timestamp,exa_field_name=time""",
    """exa_json_path=$.event_simpleName,exa_field_name=operation""",
    """exa_json_path=$.event_simpleName,exa_field_name=event_code""",
    """exa_json_path=$.aid,exa_field_name=aid""",
    """exa_json_path=$.FirewallRule,exa_field_name=additional_info""",
    """exa_json_path=$.UserName,exa_regex=(LOCAL SERVICE|(({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))|({user}[\w\.\-\!\#\^\~]{1,40}\$?)))""",
    """exa_regex=src-account-name":"({account_name}[^\"]+)""",
    """exa_json_path=$.FirewallOption,exa_field_name=action""",
    """exa_json_path=$.FirewallRuleId,exa_field_name=rule_id""",
    """exa_json_path=$.FirewallRule,exa_field_name=rule""",
    """exa_json_path=$.event_platform,exa_field_name=os""",
    """exa_json_path=$.cid,exa_field_name=cid""",
    """exa_json_path=$.LocalAddressIP4,exa_regex=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
    """exa_json_path=$.ComputerName,exa_regex=({host}[\w\-\.]+)""",
    """exa_json_path=$.aip,exa_field_name=aip"""
  ]
  ParserVersion = "v1.0.0"


}
```