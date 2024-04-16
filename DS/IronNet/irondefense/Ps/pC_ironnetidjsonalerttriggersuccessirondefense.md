#### Parser Content
```Java
{
Name = ironnet-id-json-alert-trigger-success-irondefense
  ExtractionType = json
  ParserVersion = v1.0.0
  Vendor = IronNet
  Product = IronDefense
  TimeFormat =  "yyyy-MM-dd'T'HH:mm:ssZ"
  Conditions = [ """"app":"irondefense"""", """"type":"event"""", """"alert_status":"""", """"severity":"""", """"alert_aggregation_criteria":""""  ]
  Fields = [
    """exa_json_path=$.start_time,exa_field_name=time""",
    """exa_json_path=$.subject,exa_field_name=alert_name""",
    """exa_json_path=$.src_category,exa_field_name=alert_type""",
    """exa_json_path=$.severity,exa_field_name=alert_severity""",
    """exa_json_path=$.alert_status,exa_field_name=alert_status""",
    """exa_json_path=$.src_ip,exa_regex=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
    """exa_json_path=$.dst_ip,exa_regex=({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?""",
    """exa_json_path=$.dst_port,exa_field_name=dest_port""",
    """exa_json_path=$.bytes_out,exa_field_name=bytes_out""",
    """exa_json_path=$.body,exa_field_name=additional_info""",
  ]


}
```