#### Parser Content
```Java
{
Name = microsoft-azure-json-dns-request-fail-azurefirewalldnsresolutionfailurelog
  Vendor = Microsoft
  Product = Azure Monitor
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSSSSZ"
  ExtractionType = json
  Conditions = [""""category":""", """"AzureFirewallNetworkRule"""", """"resourceId":""", """"AzureFirewallDNSResolutionFailureLog"""" ]
  Fields = [
    """exa_json_path=$.time,exa_field_name=time""",
    """exa_json_path=$.resourceId,exa_field_name=resource_id""",
    """exa_json_path=$.operationName,exa_field_name=operation""",
    """exa_json_path=$.category,exa_field_name=category""",
    """exa_json_path=$..msg,exa_field_name=additional_info""",
    """exa_json_path=$..msg,exa_regex=(Failed to resolve FQDN ({dns_query}[^\s]+)\..+?:\s+({failure_reason}[^\.]+))""",
    """exa_json_path=$..msg,exa_regex=Rule:\s*({rule}[^"]+)"""
   ]
   DupFields = [ "operation->event_name" ]
   ParserVersion = "v1.0.0"


}
```