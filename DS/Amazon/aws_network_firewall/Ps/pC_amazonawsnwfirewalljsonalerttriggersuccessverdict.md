#### Parser Content
```Java
{
Name = amazon-awsnwfirewall-json-alert-trigger-success-verdict
    Vendor = Amazon
    Product = AWS Network Firewall
    TimeFormat = "epoch"
    ParserVersion = v1.0.0
    ExtractionType = json    
    Conditions = [ """availability_zone""", """firewall_name""", """"verdict":""", """"action":"alert"""" ]
    Fields = [
       """exa_json_path=$.firewall_name,exa_field_name=firewall""",
       """exa_json_path=$.availability_zone,exa_field_name=availabilty_zone""",
       """exa_json_path=$.event_timestamp,exa_field_name=time""",
       """exa_json_path=$.event.verdict.action,exa_field_name=action""",
       """exa_json_path=$.event.src_ip,exa_regex=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))""",
       """exa_json_path=$.event.src_port,exa_field_name=src_port""",
       """exa_json_path=$.event.dest_ip,exa_regex=({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))""",
       """exa_json_path=$.event.dest_port,exa_field_name=dest_port""",       
       """exa_json_path=$.event.proto,exa_field_name=protocol""",
       """exa_json_path=$.event.pkt_src,exa_field_name=additional_info""",
       """exa_json_path=$.event.direction,exa_field_name=direction""",
       """exa_json_path=$.event.alert.severity,exa_field_name=alert_severity""",
       """exa_json_path=$.event.alert.signature,exa_field_name=alert_name""",
       """exa_json_path=$.event.alert.category,exa_field_name=alert_type"""
    ]
  

}
```