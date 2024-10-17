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
    """\"event_simpleName\":\"({operation}[^\"]+)"""
    """\"aid\":\"({aid}[^\"]+)"""
    """\"FirewallRule\":\"({additional_info}[^\"]+)"""
    """\"UserName\":\"(({email_address}[^@\"]+@[^\"]+)|({user}[\w\.\-\!\#\^\~]{1,40}\$?))\""""
    """src-account-name\":\"({account_name}[^\"]+)"""
    """"FirewallOption":"({action}[^"]+)""""
    """"FirewallRuleId":"({rule_id}[^"\s]+)""""
    """"FirewallRule":"({rule}[^"]+)","""
    """"event_platform":"({os}[^"]+)""""
    """"cid":"({cid}[^"]+)"""
    """exa_regex="hostname":"({host}[\w\-.]+)"""",
    """exa_json_path=$.timestamp,exa_field_name=time""",
    """exa_json_path=$.event_simpleName,exa_field_name=operation""",
    """exa_json_path=$.aid,exa_field_name=aid""",
    """exa_json_path=$.FirewallRule,exa_field_name=additional_info""",
    """exa_json_path=$.UserName,exa_regex=(LOCAL SERVICE|(({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))|({user}[\w\.\-\!\#\^\~]{1,40}\$?)))""",
    """exa_regex=src-account-name":"({account_name}[^\"]+)""",
    """exa_json_path=$.FirewallOption,exa_field_name=action""",
    """exa_json_path=$.FirewallRuleId,exa_field_name=rule_id""",
    """exa_json_path=$.FirewallRule,exa_field_name=rule""",
    """exa_json_path=$.event_platform,exa_field_name=os""",
    """exa_json_path=$.cid,exa_field_name=cid"""
  ]
  DupFields = [
    "operation->event_code"
  ]
  ParserVersion = "v1.0.0"


}
```