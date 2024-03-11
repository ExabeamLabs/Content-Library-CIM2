#### Parser Content
```Java
{
Name = vmware-carbonblack-json-alert-trigger-success-watchlist-1
  Vendor = VMware
  Product = Carbon Black CES
  ParserVersion = "v1.0.0"
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
  Conditions = [ """"legacy_alert_id"""", """"threat_indicators"""", """"device_username":""", """_threat_category"""", """"type":""", """"WATCHLIST"""" ]
  Fields = [
    """"+create_time"+:\s*"+({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d.\d\d\dZ)""",
    """"+severity":\s*({alert_severity}[^,]+?),""",
    """"+category"+:\s*"+({category}[^"]+?)"+""",
    """"+threat_id"+:\s*"+({threat_id}[^"]+?)"+""",
    """"+device_username"+:\s*"+(({email_address}[^@,"]+@[^",]+)|(({domain}[^\\"]+?)\\+)?({user}[^"]+))"+""",
    """"+device_name"+:\s*"+(\w+\\+)?({host}[^."]+)""",
    """"+threat_indicators":[^\}\]]*?"process_name"+:\s*"+({process_name}[^"]+?)"+""",
    """"+reason"+:\s*"+({additional_info}[^,]+?)"+,""",
    """"+threat_indicators":[^\}\]]*?"sha256"+:\s*"+({hash_sha256}[^"]+?)"+""",
    """"+policy_name"+:\s*"+({policy_name}[^"]+?)"+""",
    """"+state"+:\s*"+({state}[^"]+?)"+""",
    """"+type"+:\s*"+({alert_type}[^"]+?)"+""",
    """"+legacy_alert_id"+:\s*"+({alert_id}[^"]+?)"+""",
    """"+org_key"+:\s*"+({primary_key}[^"]+?)"+""",
    """"+threat_cause_threat_category"+:\s*"+(UNKNOWN|({result}[^"]+?))"+""",
    """"+report_name"+:\s*"+({alert_name}[^,]+?)",""",
    """"+report_id"+:\s*"+({alert_id}[^"]+?)"+""",
    """"process_name"+:"+({process_name}[^"]+)""",
    """"threat_cause_actor_name"+:"+({process_path}({process_dir}[^"]+)\\({process_name}[^"]+))"""",
  ]


}
```