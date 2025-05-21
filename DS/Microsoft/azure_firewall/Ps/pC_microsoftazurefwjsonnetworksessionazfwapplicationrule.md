#### Parser Content
```Java
{
Name = microsoft-azurefw-json-network-session-azfwapplicationrule
     ParserVersion = v1.0.0
     Conditions = [ """"category":""", """"AZFWApplicationRule"""", """Action":""", """"Rule":""" ]
     Fields = ${AzureFwTemplates.azure-firewall.Fields} [
       """"Fqdn":\s*"({web_domain}[^"]+)""""
       """"Policy":\s*"({policy_name}[^"]+)"""
       """"RuleCollection":\s*"({rule_type}[^"]+)""""
       """"RuleCollectionGroup":\s*"({rule_source}[^"]+)""""
     ]
  
azure-firewall = {
Vendor = "Microsoft"
Product = "Azure Firewall"
TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSSSSSZ"
Fields = [
  """"time":\s*"({time}\d\d\d\d\-\d\d\-\d\dT\d\d:\d\d:\d\d\.\d\d\d\d\d\d\dZ)"""
  """"category":\s*"({category}[^"]+)"""
  """"Action":\s*"({action}[^"]+)"""
  """"SourcePort":\s*({src_port}\d+)"""
  """"DestinationPort":\s*({dest_port}\d+)"""
  """"Protocol":\s*"({protocol}[^"]+)""""
  """"Rule":\s*"({rule}[^"]+)""""
  """"SourceIp":\s*"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))""""
  """"DestinationIp":\s*"({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))""""
  """"QueryType":\s*"({dns_query_type}[^"]+)""""
  """"QueryName":\s*"({dns_query}[^"]+)""""
  """Namespace:\s*(|({event_hub_namespace}[^\]]+?))\s*\[\];\]"""
  """EventHub name:\s*(|({event_hub_name}[^\]]+?))\s*\]"""
  
}
```