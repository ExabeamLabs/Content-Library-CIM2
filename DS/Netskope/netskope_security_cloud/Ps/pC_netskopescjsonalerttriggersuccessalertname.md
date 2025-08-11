#### Parser Content
```Java
{
Name = netskope-sc-json-alert-trigger-success-alertname
  Vendor = Netskope
  Product = Netskope Security Cloud
  ParserVersion = "v1.0.0"
  TimeFormat = "epoch_sec"
  ExtractionType = json
  Conditions = [ """"alert_type": """, """"alert": "yes"""", """"alert_name":"""]
  Fields = [
    """exa_json_path=$.timestamp,exa_field_name=time"""
    """exa_json_path=$.hostname,exa_field_name=dest_host"""
    """exa_json_path=$.policy,exa_field_name=alert_name"""
    """exa_json_path=$.alert_type,exa_field_name=alert_type"""
    """exa_json_path=$.dstip,exa_regex=({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?"""
    """exa_json_path=$.url,exa_field_name=malware_url"""
    """exa_json_path=$.alert_name,exa_field_name=alert_name"""
    """exa_json_path=$.internal_id,exa_field_name=alert_id"""
    """exa_json_path=$.category,exa_field_name=additional_info"""
    """exa_json_path=$.srcip,exa_regex=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
    """exa_json_path=$.user,exa_regex=(unknown|(({email_address}[^"@\\\/\s]+@({domain}[^.]+)[^"]+)))"""
    """exa_json_path=$.activity,exa_field_name=operation"""
    """exa_json_path=$.src_country,exa_field_name=country"""
    """exa_json_path=$.os,exa_regex=((U|u)nknown|({os}[^"]+))"""
    """exa_json_path=$.browser,exa_regex=((U|u)nknown|({browser}[^"]+))"""
    """exa_regex="page":\s*"({web_domain}[^"\/]+)"""
    """exa_json_path=$.dst_location,exa_field_name=location"""
    """exa_json_path=$.app,exa_field_name=app"""
    """exa_json_path=$.md5,exa_field_name=hash_md5"""
    """exa_json_path=$.from_user,exa_field_name=from_user_at"""
    """exa_json_path=$.file_path,exa_field_name=file_path_at"""
    """exa_json_path=$.shared_with,exa_field_name=shared_with_at"""
    """exa_json_path=$.site,exa_field_name=site_at"""
    """exa_json_path=$.protocol,exa_field_name=protocol"""
    """exa_json_path=$.domain,exa_field_name=web_domain"""
    """exa_json_path=$.file_size,exa_field_name=bytes"""
    """exa_json_path=$.shared_domains,exa_regex=[\[\<\s]?({domain}[^"\s,\\\]\>]+)"""
    """exa_json_path=$.computer_name,exa_field_name=host"""
    """exa_json_path=$.severity,exa_field_name=alert_severity"""
    """exa_json_path=$.domain,exa_field_name=domain"""
    """"alert_name":\s*"({alert_name}[^",]+)"""
    """"alert_type":\s*"({alert_type}[^",]+)"""
    """"severity":\s*"({alert_severity}[^",]+)"""
    """"action":\s*"({action}[^",]+)"""
    """"activity":\s*"({operation}[^",]+)"""
    """"category":\s*"({category}[^",]+)"""
    """"dstport":\s*({dest_port}\d+)"""
    """"srcport":\s*({src_port}\d+)"""
    """"useragent":\s*"({user_agent}[^",]+)"""
    """"useragent":\s*"({user_agent}.+?)","""
    """"userip":\s*"({src_ip}[^",]+)"""
    """"dstip":\s*"({dest_ip}[^",]+)"""
    """"hostname":\s*"({dest_host}[^",]+)"""
    """"os":\s*"({os}[^",]+)"""
    """"src_country":\s*"({src_country}[^",]+)"""
    """"os_version":\s*"({os_version}[^",]+)"""
    """"dst_country":\s*"({dest_country}[^",]+)"""
    """"browser":\s*"({browser}[^",]+)"""
    """"app":\s*"({app}[^",]+)"""
    """"file_size":\s*({bytes}\d+)"""
    """"protocol":\s*"({protocol}[^",]+)"""
    """"timestamp":\s*({time}\d{10})"""
    """"md5":\s*"({hash_md5}[^",]+)"""
    """"file_type":\s*"({file_type}[^",]+)"""
    """"policy":\s*"({policy_name}[^",]+)"""
    """"shared_domains":\s*"[\[\<\s]?({domain}[^"\s,\\\]\>]+)"""
    """"computer_name":\s*"({host}[^",]+)"""    
  ]
  DupFields = [
"alert_name"->"alert_subject"
  ]


}
```