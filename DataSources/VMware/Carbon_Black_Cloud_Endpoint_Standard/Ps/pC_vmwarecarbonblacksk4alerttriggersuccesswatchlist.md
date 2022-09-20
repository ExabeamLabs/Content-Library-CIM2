#### Parser Content
```Java
{
Name = vmware-carbonblack-sk4-alert-trigger-success-watchlist
  Vendor = VMware
  Product = Carbon Black Cloud Endpoint Standard
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ssZ"
  Conditions = [ """"Carbon Black"""", """"threat_id"""", """"threat_cause_actor_name"""", """"type":"WATCHLIST"""" ]
  Fields = [
    """"+create_time"+:\s*"+({time}[^"]+?)"+""",
    """"+severity":\s*({alert_severity}[^,]+?),""",
    """"+category"+:\s*"+({category}[^"]+?)"+""",
    """"+threat_id"+:\s*"+({threat_id}[^"]+?)"+""",
    """"+device_username"+:\s*"+(({email_address}[^@,"]+@[^",]+)|(({domain}[^\"]+?)\\+)?({user}[^"]+))"+""",
    """"+device_name"+:\s*"+(\w+\\+)?({host}[^."]+)""",
    """"+threat_indicators":[^\}\]]*?"process_name"+:\s*"+({process_name}[^"]+?)"+""",
    """"+reason"+:\s*"+({additional_info}[^,]+?)"+,""",
    """"+threat_indicators":[^\}\]]*?"sha256"+:\s*"+({hash_sha256}[^"]+?)"+""",
    """"+threat_indicators"+:[^\}\]]*?"+ttps"+:\s*\["+({dest_process}[^"]+?)"+\]""",
    """"+policy_name"+:\s*"+({policy_name}[^"]+?)"+""",
    """"+state"+:\s*"+({state}[^"]+?)"+""",
    """"+type"+:\s*"+({alert_type}[^"]+?)"+""",
    """"+legacy_alert_id"+:\s*"+({alert_id}[^"]+?)"+""",
    """"+org_key"+:\s*"+({primary_key}[^"]+?)"+""",
    """"+threat_cause_threat_category"+:\s*"+(UNKNOWN|({result}[^"]+?))"+""",
    """"+report_name"+:\s*"+({alert_name}[^,]+?)",""",
    """"+report_id"+:\s*"+({alert_id}[^"]+?)"+""",
    """"process_name"+:"+({process_name}[^"]+)""",
    """"threat_cause_actor_name"+:"+({dest_process}({process_dir}[^"]+)\\({process_name}[^"]+))"""",
    """device_internal_ip"+:"+({src_ip}[A-Fa-f.:\d]+)"""
  ]
  ParserVersion = "v1.0.0"


}
```