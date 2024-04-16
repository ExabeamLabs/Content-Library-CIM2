#### Parser Content
```Java
{
Name = nozomi-guardian-json-alert-trigger-success-n2os
    Vendor = Nozomi Networks
    Product = Nozomi Networks Guardian
    ExtractionType = json
    ParserVersion = "v1.0.0"
    TimeFormat = "yyyy-MM-dd'T'HH:mm:ssZ"
    Conditions = [""""vendor_product":"Nozomi_Networks_N2OS"""", """"nozomi_source":"alerts"""", """"category":"""]
    Fields = [
      """exa_json_path=$._time,exa_field_name=time"""
      """exa_json_path=$.dvc_host,exa_field_name=host"""
      """exa_json_path=$.nozomi_type_id,exa_field_name=alert_type"""
      """exa_json_path=$.category,exa_field_name=alert_name"""
      """exa_json_path=$.nozomi_id,exa_field_name=alert_id"""
      """exa_json_path=$.description,exa_field_name=additional_info"""
      """exa_json_path=$.src_ip,exa_regex=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))"""
      """exa_json_path=$.dest_ip,exa_regex=({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))"""
      """exa_json_path=$.src_mac,exa_field_name=src_mac"""
      """exa_json_path=$.dest_mac,exa_field_name=dest_mac"""
      """exa_json_path=$.src_port,exa_field_name=src_port"""
      """exa_json_path=$.dest_port,exa_field_name=dest_port"""
      """exa_json_path=$.dest_host,exa_field_name=dest_host"""
      """exa_json_path=$.severity,exa_field_name=alert_severity"""
     ]


}
```