#### Parser Content
```Java
{
Name = cisco-firepower-json-app-activity-appactivity
  ParserVersion = "v1.0.0"
  Vendor = Cisco
  Product = Cisco Firepower
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
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
  ]
  DupFields = [ "policy_name->alert_name" ]


}
```