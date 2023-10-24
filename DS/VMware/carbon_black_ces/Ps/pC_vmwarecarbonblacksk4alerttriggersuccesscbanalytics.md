#### Parser Content
```Java
{
Name = vmware-carbonblack-sk4-alert-trigger-success-cbanalytics
  Vendor = VMware
  Product = Carbon Black CES
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ssZ"
  Conditions = [ """legacy_alert_id""", """threat_indicators""", """reason_code""", """_threat_category""", """"type":"CB_ANALYTICS"""" ]
  Fields = [
    """carbonblack,"({host}[^"]+?)"""",
    """"+create_time"+:\s*"+({time}[^"]+?)"+""",
    """"+severity":\s*({alert_severity}[^,]+?),""",
    """"+category"+:\s*"+({category}[^"]+?)"+""",
    """"+threat_id"+:\s*"+({threat_id}[^"]+?)"+""",
    """"+device_username"+:\s*"+(({email_address}[^@,"]+@[^",]+)|(({domain}[^"]+?)\\+)?({user}[\w\.\-]{1,40}\$?))"+""",
    """"+device_name"+:\s*"+(\w+\\+)?({host}[^."]+)""",
    """"+reason_code"+:\s*"+({alert_name}[^,]+?)",""",
    """"+threat_indicators":[^\}\]]*?"process_name"+:\s*"+({process_name}[^"]+?)"+""",
    """"+reason"+:\s*"+({additional_info}[^"]+?)"+""",
    """"+threat_indicators":[^\}\]]*?"sha256"+:\s*"+({hash_sha256}[^"]+?)"+""",
    """"+threat_indicators"+:[^\}\]]*?"+ttps"+:\s*\["+({dest_process}[^"]+?)"+\]""",
    """"+policy_name"+:\s*"+({policy_name}[^"]+?)"+""",
    """"+state"+:\s*"+({state}[^"]+?)"+""",
    """"+type"+:\s*"+({alert_type}[^"]+?)"+""",
    """"+legacy_alert_id"+:\s*"+({alert_id}[^"]+?)"+""",
    """"+org_key"+:\s*"+({primary_key}[^"]+?)"+""",
    """"+not_blocked_threat_category"+:\s*"+(UNKNOWN|({result}[^"]+?))"+""",
    """"+blocked_threat_category"+:\s*"+(UNKNOWN|({result}[^"]+?))"+""",
    """"+report_name"+:\s*"+({alert_name}[^,]+?)",""",
    """"+not_blocked_threat_category"+:\s*"+(UNKNOWN|({alert_type}[^"]+?))"+""",
    """"+report_id"+:\s*"+({alert_id}[^"]+?)"+""",
    """"process_name"+:"+({process_name}[^"]+)""",
    """"threat_cause_actor_name"+:"+({dest_process}({process_dir}[^"]+)\\({process_name}[^"]+))"""",
    """device_internal_ip"+:"+({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
  ]
  ParserVersion = "v1.0.0"


}
```