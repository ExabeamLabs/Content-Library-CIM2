#### Parser Content
```Java
{
Name = tanium-cp-json-alert-trigger-success-security
    ExtractionType = json
    Vendor = Tanium
    Product = Tanium Core Platform
    ParserVersion = "v1.0.0"
    TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
    Conditions = [ """tanium-index""", """Timestamp""", """Computer Name""", """Computer IP""" ]
    Fields = [
      """"Timestamp":"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d.\d\d\dZ)"""",
      """"User Name":"({user}[\w\.\-]{1,40}\$?)"""",
      """"User Id":"({user}[\w\.\-]{1,40}\$?)"""",
      """"User Domain":"({domain}[^",]+?)"""",
      """"user\\*":\\*"((NT AUTHORITY|({domain}[^"\\]+))\\+)?(SYSTEM|({user}[\w\.\-]{1,40}\$?))\\*"""",
      """"Priority":"({alert_severity}[^",]+)"""",
      """"Event Name":"({alert_name}[^",]+)"""",
      """({alert_name}Reputation Malicious Files)""",
      """"Event Name":"({alert_type}[^",]+)"""",
      """"type\\*":\\*"({alert_type}[^"]+?)\\*"""",
      """"Event Id":"({alert_id}[^",]+)"""",
      """"Computer Name":"({src_host}[^"]+?)"""",
      """"Computer IP":"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""",
      """"fullpath\\*":\\*"({malware_url}[^"]+?)\\*"""",
      """"name\\*":\\*"({file_name}[^"]+?)\\*"""",
      """"source\\*":\\*"({log_source}[^"]+?)\\*"""",
      """properties"+:[^\]]+?fullpath"+:"+({process_path}({process_dir}[^"]+)\\+({process_name}[^"]+))""",
      """exa_json_path=$.['Event Id'],exa_field_name=alert_id"""
    """exa_json_path=$.Timestamp,exa_field_name=time"""
    """exa_json_path=$.['User Name'],exa_field_name=user"""
    """exa_json_path=$.['User Id'],exa_field_name=user"""
    """exa_json_path=$.['User Domain'],exa_field_name=domain"""
    """exa_json_path=$.Priority,exa_field_name=alert_severity"""
    """exa_json_path=$.['Event Name'],exa_field_name=alert_name"""
    """exa_json_path=$.['Event Name'],exa_field_name=alert_type"""
    """exa_json_path=$.['Computer Name'],exa_field_name=src_host"""
    """exa_json_path=$.['Other Parameters'],exa_regex="fullpath\\":\\"({malware_url}[^"]+?)\\*"""
    """exa_json_path=$.['Other Parameters'],exa_regex="name\\":\\"({file_name}[^"]+?)\\*""""
    """exa_json_path=$.['Other Parameters'],exa_regex="type\\":\\"({alert_type}[^"]+?)\\*""""
    """exa_json_path=$.['Other Parameters'],exa_regex="name\\":\\"({file_name}[^"]+?)\\*""""
    """exa_json_path=$.['Other Parameters'],exa_regex="source\\":\\"({log_source}[^"]+?)\\*""""
    """exa_regex=({alert_name}Reputation Malicious Files)"""

    ]


}
```