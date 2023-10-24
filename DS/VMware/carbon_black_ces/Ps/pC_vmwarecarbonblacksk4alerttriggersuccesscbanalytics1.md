#### Parser Content
```Java
{
Name = vmware-carbonblack-sk4-alert-trigger-success-cbanalytics-1
  Vendor = VMware
  Product = Carbon Black CES
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
  Conditions = [ """"type":"CB_ANALYTICS"""", """"reason_code"""", """"alert_url":""", """"threat_id":""", """"device_username":""" ]
  Fields = [
    """"detection_timestamp"+:"+({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d{3}Z)""",
    """"type"+:"+({alert_type}[^"]+)"""",
    """"reason_code"+:"+({alert_name}[^"]+)"""",
    """"threat_id"+:"+({threat_id}[^"]+)"""",
    """"severity"+:({alert_severity}\d+)""",
    """"reason"+:"+({alert_reason}[^,]+)"+,""",
    """"alert_url"+:"+({url}[^"]+)"""",
    """"process_name"+:"+({process_path}(({process_dir}[^",]+?)[\\\/]+)?({process_name}[^\/\\"]+))"""",
    """"process_cmdline"+:"+({process_command_line}.+?)"+,""",
    """"parent_name"+:"+({parent_process}({parent_process_dir}[^"]*?[\\\/]+)?({parent_process_name}[^"\\\/]+))"""",
    """"org_key"+:"+({primary_key}[^"]+)"""",
    """"device_name"+:"+(\w+\\+)?({host}[\w\-.]+)"""",
    """"device_internal_ip"+:"+({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""",
    """"device_username"+:"+(({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))|(({domain}[^"]+?)\\+)?({user}[\w\.\-]{1,40}\$?))"""",
    """"process_username"+:"+(NT AUTHORITY\\+(SYSTEM|NETWORK SERVICE|LOCAL SERVICE)|(({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))|(({domain}[^"]+?)\\+)?({user}[\w\.\-]{1,40}\$?)))"""",
    """"device_os"+:"+({os}[^"]+)""""
  ]
  DupFields = [ "threat_id->alert_id" ]
  ParserVersion = "v1.0.0"


}
```