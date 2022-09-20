#### Parser Content
```Java
{
Name = tanium-ep-json-alert-trigger-success-security
    Vendor = Tanium
    Product = Endpoint Platform
    ParserVersion = "v1.0.0"
    TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
    Conditions = [ """tanium-index""", """Timestamp""", """Computer Name""", """Computer IP""" ]
    Fields = [
      """"Timestamp":"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d.\d\d\dZ)"""",
      """"User Name":"({user}[^",]+?)"""",
      """"User Id":"({user}[^",]+?)"""",
      """"User Domain":"({domain}[^",]+?)"""",
      """"user\\*":\\*"((NT AUTHORITY|({domain}[^"\\]+))\\+)?(SYSTEM|({user}[^"]+?))\\*"""",
      """"Priority":"({alert_severity}[^",]+)"""",
      """"Event Name":"({alert_name}[^",]+)"""",
      """({alert_name}Reputation Malicious Files)""",
      """"Event Name":"({alert_type}[^",]+)"""",
      """"type\\*":\\*"({alert_type}[^"]+?)\\*"""",
      """"Event Id":"({alert_id}[^",]+)"""",
      """"Computer Name":"({src_host}[^"]+?)"""",
      """"Computer IP":"({src_ip}[a-fA-F\d.:]+)"""",
      """"fullpath\\*":\\*"({malware_url}[^"]+?)\\*"""",
      """"name\\*":\\*"({file_name}[^"]+?)\\*"""",
      """"source\\*":\\*"({log_source}[^"]+?)\\*"""",
      """properties"+:[^\]]+?fullpath"+:"+({process_path}({process_dir}[^"]+)\\+({process_name}[^"]+))""",
    ]
  

}
```