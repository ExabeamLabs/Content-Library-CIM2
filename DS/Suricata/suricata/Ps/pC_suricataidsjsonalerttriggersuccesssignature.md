#### Parser Content
```Java
{
Name = "suricata-ids-json-alert-trigger-success-signature"
ExtractionType = json
Vendor = "Suricata"
Product = "Suricata"
TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSSSSZ"
Conditions = [
"""flow_id"""
"""event_type"""
"""community_id"""
"""action"""
"""signature"""
"""category"""
]
Fields = [
""""timestamp\\?":\\?"({time}\d+-\d+-\d+T\d+:\d+:\d+.\d+\+\d+)"""
"""exa_json_path=$.message,exa_regex="timestamp\\?":\\?"({time}\d+-\d+-\d+T\d+:\d+:\d+.\d+\+\d+)"""
"""exa_json_path=$.message,exa_regex="src_ip\\?":\\?"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
"""exa_json_path=$.message,exa_regex="src_port\\?":\\?({src_port}\d+)"""
"""exa_json_path=$.message,exa_regex="dest_ip\\?":\\?"({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?"""
"""exa_json_path=$.message,exa_regex="dest_port\\?":\\?({dest_port}\d+)"""
"""exa_json_path=$.message,exa_regex="proto\\?":\\?"({protocol}[^""\\]+)"""
"""exa_json_path=$.message,exa_regex="flow_id\\?":\\?({alert_id}\d+)"""
"""exa_json_path=$.message,exa_regex="severity\\?":\\?({alert_severity}\d+)"""
"""exa_json_path=$.message,exa_regex="signature\\?":\s*\\"({rule}[^\\"]+)\\""""
"""exa_json_path=$.message,exa_regex="action\\":\s*"\\({action}[^\\"]+)"""
"""exa_json_path=$.category,exa_field_name=alert_type"""
"""exa_json_path=$.message,exa_regex="rule\\?":\s*\\?"({rule}[^\\"]+)\s\("""
"""exa_json_path=$.message,exa_regex="signature_id\\?":\s*\\({rule_id}\d+)"""
"""exa_json_path=$.host.name,exa_field_name=host"""
"""exa_json_path=$.message,exa_regex="payload_printable\\":\\"({payload_printable}[^,]+)\\","""
"""exa_json_path=$.message,exa_regex=msg:\\+"*({alert_name}[^"\\]+)"""
"""exa_json_path=$.message,exa_regex="app_proto\\":\\"({app_protocol}[^\\"]+)"""
"""exa_json_path=$.category,exa_field_name=category"""
"""exa_json_path=$.message,exa_regex="category\\?":\\?"({alert_type}[^\\"]+)"""
]
ParserVersion = "v1.0.0"


}
```