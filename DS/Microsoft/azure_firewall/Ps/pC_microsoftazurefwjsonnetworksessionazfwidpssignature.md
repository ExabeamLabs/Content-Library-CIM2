#### Parser Content
```Java
{
Name = microsoft-azurefw-json-network-session-azfwidpssignature
     ParserVersion = v1.0.0
     Conditions = [ """"category":"AZFWIdpsSignature"""", """Action":""", """"Category":"""]
     Fields = ${AzureFwTemplates.azure-firewall.Fields} [
       """"Policy":"({policy_name}[^"]+)"""
       """"Description":"({additional_info}[^"]+)"""
       """"Severity"+:({severity}\d+)"""
     ]
  
azure-firewall = {
Vendor = "Microsoft"
Product = "Azure Firewall"
TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSSSSSZ"
Fields = [
  """"time":"({time}\d\d\d\d\-\d\d\-\d\dT\d\d:\d\d:\d\d\.\d\d\d\d\d\d\dZ)"""
  """"category":"({category}[^"]+)"""
  """"Action":"({action}[^"]+)"""
  """"SourcePort":({src_port}\d+)"""
  """"DestinationPort":({dest_port}\d+)"""
  """"Protocol":"({protocol}[^"]+)""""
  """"Rule":"({rule}[^"]+)""""
  """"SourceIp":"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))""""
  """"DestinationIp":"({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))""""
  """"QueryType":"({dns_query_type}[^"]+)""""
  """"QueryName":"({dns_query}[^"]+)""""
  """Namespace:\s*(|({event_hub_namespace}[^\]]+?))\s*\[\];\]"""
  """EventHub name:\s*(|({event_hub_name}[^\]]+?))\s*\]"""
  
}
```