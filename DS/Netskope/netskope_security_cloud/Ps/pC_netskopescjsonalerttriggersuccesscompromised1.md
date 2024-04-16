#### Parser Content
```Java
{
Name = netskope-sc-json-alert-trigger-success-compromised-1
  ParserVersion = v1.0.0
  Product = Netskope Security Cloud
  Conditions = [ """"alert_type":"Compromised Credential"""",""""alert":"yes"""", """"type":"breach"""" ,""""alert_name":"""" ]
   Fields = ${NetskopeParsersTemplates.json-netskope-alert.Fields}[
    """exa_json_path=$.breach_description,exa_field_name=additional_info"""
    """exa_json_path=$.breach_id,exa_field_name=alert_id"""
  ]

json-netskope-alert = {
  Vendor = Netskope
  Product = Netskope Security Cloud
  ExtractionType = json
  TimeFormat = "epoch_sec"
  Fields = [
    """exa_json_path=$.timestamp,exa_field_name=time"""
    """exa_json_path=$.hostname,exa_field_name=host"""
    """exa_json_path=$.incident_id,exa_field_name=alert_id"""
    """exa_json_path=$.srcip,exa_regex=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
    """exa_json_path=$.dstip,exa_regex=({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?"""
    """exa_json_path=$.dsthost,exa_field_name=dest_host"""
    """exa_json_path=$.alert_type,exa_field_name=alert_type"""
    """exa_json_path=$.useragent,exa_field_name=user_agent"""
    """exa_json_path=$.protocol,exa_field_name=protocol"""
    """exa_json_path=$.user,exa_regex=(({email_address}([A-Za-z0-9]+[!#$%&'+-\/=?^_`~])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+))|({user}[\w\.\-]{1,40}\$?))"""
    """exa_json_path=$.severity,exa_regex=(unknown|({alert_severity}[^"]+))"""
    """exa_json_path=$.numbytes,exa_field_name=bytes"""
    """exa_regex="page":\s*"({web_domain}[^\\\/"]+)"""
    """exa_json_path=$.url,exa_field_name=malware_url"""
  ]
 DupFields = [ "alert_type->alert_name" 
}
```