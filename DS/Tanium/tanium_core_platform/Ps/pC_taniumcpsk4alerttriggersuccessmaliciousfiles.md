#### Parser Content
```Java
{
Name = "tanium-cp-sk4-alert-trigger-success-maliciousfiles"
  Vendor = "Tanium"
  Product = "Tanium Core Platform"
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
  Conditions = [
   """Computer Name"""
   """Computer IP"""
   """Intel Type"""
   """Reputation Malicious Files"""
   """md5"""
  ]
  Fields = [
    """Timestamp"+:"+({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d\d\dZ)"""
    """Alert Id"+:"+({alert_id}[^"]+)"""
    """Computer Name"+:"+({src_host}[^".]+)"""
    """Computer IP"+:"+({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
    """({alert_name}Reputation Malicious Files)"""
    """Intel Type"+:"+({alert_type}[^"]+)"""
    """properties"+:[^\]]+?fullpath"+:"+({process_path}({process_dir}[^"]+)\\+({process_name}[^"]+))"""
    """md5"+:"+({hash_md5}[^"]+)"""
    """os"+:"+({os}[^"]+)"""
    """suser=(anonymous|({user}[\w\.\-]{1,40}\$?))"""
    """({app}Tanium)"""
  ]
  ParserVersion = "v1.0.0"


}
```