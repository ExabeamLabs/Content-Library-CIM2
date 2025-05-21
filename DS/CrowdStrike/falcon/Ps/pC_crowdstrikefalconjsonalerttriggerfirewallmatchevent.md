#### Parser Content
```Java
{
Name = crowdstrike-falcon-json-alert-trigger-firewallmatchevent
  ParserVersion = "v1.0.0"
  ExtractionType = json
  Conditions = [ """"offset":""", """"eventType":""", """"FirewallMatchEvent"""", """"RuleName"""" ]

json-crowdstrike-alert-1 = {
  Vendor = CrowdStrike
  Product = Falcon
  ExtractionType = json
  TimeFormat = ["yyyy-MM-dd'T'HH:mm:ssZ","epoch"]
  Fields = [
    """"Timestamp":\s*"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\dZ)""",
# customer_id is removed
    """"EventType":\s*"({event_name}[^"]+)""",
    """"ConnectionDirection":\s*"({direction}\d+)""",
    """"HostName":\s*"({host}[^"]+)""",
    """"LocalAddress":\s*"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
    """"LocalPort":\s*"({src_port}\d+)""",
    """"PolicyName":\s*"({policy_name}[^"]+)""",
    """"Protocol":\s*"({protocol}[^"]+)""",
    """"RemoteAddress":\s*"({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?""",
    """"RemotePort":\s*"({dest_port}\d+)""",
    """"RuleAction":\s*"({action}\d+)""",
    """"RuleName":"({rule}[^"]+)""",
    """"cid":"({cid}[^"]+)""""
    """"customerIDString":"({cid}[^"]+)""""
    """"LocalAddressIP(4|6)":\s*"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))",.+?"LocalPort":\s*"({src_port}\d+)".+?"ConnectionDirection":"0"""",
    """"LocalAddressIP(4|6)":\s*"({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))",.+?"LocalPort":"({dest_port}\d+)".+?"ConnectionDirection":"1"""",
    """"RemoteAddressIP(4|6)":\s*"({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))",.+?"RemotePort":"({dest_port}\d+)".+?"ConnectionDirection":"0"""",
    """"RemoteAddressIP(4|6)":\s*"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))",.+?"RemotePort":\s*"({src_port}\d+)".+?"ConnectionDirection":"1"""",
    """exa_json_path=$.event.Timestamp,exa_field_name=time""",
    """exa_json_path=$..eventType,exa_field_name=event_name""",
    """exa_json_path=$.event.EventType,exa_field_name=event_name""",
    """exa_json_path=$.event.ConnectionDirection,exa_field_name=direction""",
    """exa_json_path=$.event.HostName,exa_field_name=host""",
    """exa_json_path=$.event.LocalAddress,exa_regex=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
    """exa_json_path=$.event.LocalPort,exa_field_name=src_port""",
    """exa_json_path=$.event.RemoteAddress,exa_regex=({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?""",
    """exa_json_path=$.event.RemotePort,exa_field_name=dest_port""",
    """exa_json_path=$.event.PolicyName,exa_field_name=policy_name""",
    """exa_json_path=$.event.Protocol,exa_field_name=protocol""",
    """exa_json_path=$.event.RuleAction,exa_field_name=action""",
    """exa_json_path=$.event.RuleName,exa_field_name=rule""",
    """exa_json_path=$..cid,exa_field_name=cid""",
    """exa_json_path=$..customerIDString,exa_field_name=cid""",
    """exa_regex="LocalAddressIP(4|6)":"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))",.+?"LocalPort":"({src_port}\d+)".+?"ConnectionDirection":"0"""",
    """exa_regex="LocalAddressIP(4|6)":"({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))",.+?"LocalPort":"({dest_port}\d+)".+?"ConnectionDirection":"1"""",
    """exa_regex="RemoteAddressIP(4|6)":"({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))",.+?"RemotePort":"({dest_port}\d+)".+?"ConnectionDirection":"0"""",
    """exa_regex="RemoteAddressIP(4|6)":"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))",.+?"RemotePort":"({src_port}\d+)".+?"ConnectionDirection":"1""""
  
}
```