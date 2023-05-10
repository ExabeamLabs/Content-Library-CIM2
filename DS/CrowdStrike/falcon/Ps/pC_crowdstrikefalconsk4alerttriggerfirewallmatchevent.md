#### Parser Content
```Java
{
Name = crowdstrike-falcon-sk4-alert-trigger-firewallmatchevent
  Vendor = CrowdStrike
  Product = Falcon
  ParserVersion = "v1.0.0"
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ssZ"
  Conditions = [ """"offset":""", """destinationServiceName =CrowdStrike""", """"eventType":"FirewallMatchEvent"""", """"RuleName"""" ]
  Fields = [
    """"Timestamp":"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\dZ)""",
# customer_id is removed
    """"EventType":"({event_name}[^"]+)""",
    """"ConnectionDirection":"({direction}\d+)""",
    """"HostName":"({host}[^"]+)""",
    """"LocalAddress":"({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
    """"LocalPort":"({src_port}\d+)""",
    """"PolicyName":"({policy_name}[^"]+)""",
    """"Protocol":"({protocol}[^"]+)""",
    """"RemoteAddress":"({dest_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?""",
    """"RemotePort":"({dest_port}\d+)""",
    """"RuleAction":"({action}\d+)""",
    """"RuleName":"({rule}[^"]+)"""
  ]


}
```