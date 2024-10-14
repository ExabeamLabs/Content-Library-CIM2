#### Parser Content
```Java
{
Name = netskope-sc-json-alert-trigger-success-alertname-1
  Vendor = Netskope
  Product = Netskope Security Cloud
  ParserVersion = "v1.0.0"
  TimeFormat = "epoch_sec"
  ExtractionType = json
  Conditions = [ """"alert_type":"ctep"""", """"alert":"yes"""", """"alert_name":""" ]
  Fields = [
    """exa_json_path=$.timestamp,exa_field_name=time"""
    """exa_json_path=$.hostname,exa_field_name=dest_host"""
    """exa_json_path=$.alert_type,exa_field_name=alert_type"""
    """exa_json_path=$.dstip,exa_regex=({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?"""
    """exa_json_path=$.url,exa_field_name=malware_url"""
    """exa_json_path=$.alert_name,exa_field_name=alert_name"""
    """exa_json_path=$._id,exa_field_name=alert_id"""
    """exa_json_path=$.category,exa_field_name=additional_info"""
    """exa_json_path=$.srcip,exa_regex=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
    """exa_json_path=$.user,exa_regex=(unknown|(({email_address}[^"@\\\/\s]+@({domain}[^.]+)[^"]+)))"""
    """exa_json_path=$.src_country,exa_field_name=country"""
    """exa_json_path=$.os,exa_regex=((U|u)nknown|({os}[^"]+))"""
    """exa_json_path=$.dst_location,exa_field_name=location"""
    """exa_json_path=$.app,exa_field_name=app"""
    """exa_json_path=$.site,exa_field_name=site_at"""
    """exa_json_path=$.ip_protocol,exa_field_name=protocol"""
  ]
  DupFields = [
"alert_name"->"alert_subject"
  ]


}
```