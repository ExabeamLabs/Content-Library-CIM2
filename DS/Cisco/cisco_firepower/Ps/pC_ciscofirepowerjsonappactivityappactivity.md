#### Parser Content
```Java
{
Name = cisco-firepower-json-app-activity-appactivity
  ParserVersion = "v1.0.0"
  Vendor = Cisco
  Product = Cisco Firepower
  ExtractionType = json
  TimeFormat = [ "yyyy-MM-dd'T'HH:mm:ss","MMM dd HH:mm:ss" ]
  Conditions = [ """"@computed":""", """"recordTypeCategory":""", """"recordTypeDescription":""" ]
  Fields = [
    """\WeventDateTime":\s*"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)""",
    """\WrecordTypeDescription":\s*"({policy_name}[^"]+)""",
    """\Wdata":\s*"(N\/A|({event_name}[^"]+))""",
    """\WfirewallRuleReason":\s*"(N\/A|({event_name}[^"]+))""",
    """\WrecordTypeCategory":\s*"({alert_type}[^"]+)""",
    """\Wsensor":\s*"({sensor}[^"]+)""",
    """"sourceIpv6Address":\s*"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
    """"destinationIpv6Address":\s*"({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?""",
    """({time}\w{3}\s\d\d\s\d\d:\d\d:\d\d)\s""",
    """exa_json_path=$.@computed.eventDateTime,exa_field_name=time""",
    """exa_json_path=$.@computed.recordTypeDescription,exa_field_name=policy_name""",
    """exa_json_path=$.eventDescription.data,exa_field_name=event_name""",
    """exa_regex=\WfirewallRuleReason":\s*"(N\/A|({event_name}[^"]+))""",
    """exa_json_path=$.@computed.recordTypeCategory,exa_field_name=alert_type""",
    """exa_json_path=$.@computed.sensor,exa_field_name=sensor""",
    """exa_json_path=$.sourceIpv6Address,exa_regex=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
    """exa_json_path=$.destinationIpv6Address,exa_regex=({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?""",
  ]
  DupFields = [ "policy_name->alert_name" ]


}
```