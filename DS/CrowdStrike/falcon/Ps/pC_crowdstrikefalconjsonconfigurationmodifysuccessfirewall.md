#### Parser Content
```Java
{
Name = "crowdstrike-falcon-json-configuration-modify-success-firewall"
  Vendor = "CrowdStrike"
  Product = "Falcon"
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
    """\"UserName\":\"(({email_address}[^@\"]+@[^\"]+)|({user}[\w\.\-]{1,40}\$?))\""""
    """src-account-name\":\"({account_name}[^\"]+)"""
    """"FirewallOption":"({action}[^"]+)""""
    """"FirewallRuleId":"({rule_id}[^"\s]+)""""
    """"FirewallRule":"({rule}[^"]+)","""
    """"event_platform":"({os}[^"]+)""""
    """"cid":"({cid}[^"]+)"""
  ]
  DupFields = [
    "operation->event_code"
  ]
  ParserVersion = "v1.0.0"


}
```