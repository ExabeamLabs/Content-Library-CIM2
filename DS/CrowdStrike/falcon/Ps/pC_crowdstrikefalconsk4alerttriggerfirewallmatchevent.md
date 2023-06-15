#### Parser Content
```Java
{
Name = crowdstrike-falcon-sk4-alert-trigger-firewallmatchevent
  ParserVersion = "v1.0.0"
  Conditions = [ """"offset":""", """destinationServiceName =CrowdStrike""", """"eventType":"FirewallMatchEvent"""", """"RuleName"""" ]

json-crowdstrike-alert-1 = {
  Vendor = CrowdStrike
  Product = Falcon
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ssZ"
  Fields = [
    """"Timestamp":"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\dZ)""",
# customer_id is removed
    """"EventType":"({event_name}[^"]+)""",
    """"ConnectionDirection":"({direction}\d+)""",
    """"HostName":"({host}[^"]+)""",
    """"LocalAddress":"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
    """"LocalPort":"({src_port}\d+)""",
    """"PolicyName":"({policy_name}[^"]+)""",
    """"Protocol":"({protocol}[^"]+)""",
    """"RemoteAddress":"({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?""",
    """"RemotePort":"({dest_port}\d+)""",
    """"RuleAction":"({action}\d+)""",
    """"RuleName":"({rule}[^"]+)""",
    """"LocalAddressIP(4|6)":"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))",.+?"LocalPort":"({src_port}\d+)".+?"ConnectionDirection":"0"""",
""""LocalAddressIP(4|6)":"({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))",.+?"LocalPort":"({dest_port}\d+)".+?"ConnectionDirection":"1"""",
""""RemoteAddressIP(4|6)":"({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))",.+?"RemotePort":"({dest_port}\d+)".+?"ConnectionDirection":"0"""",
""""RemoteAddressIP(4|6)":"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))",.+?"RemotePort":"({src_port}\d+)".+?"ConnectionDirection":"1""""
  
}
```