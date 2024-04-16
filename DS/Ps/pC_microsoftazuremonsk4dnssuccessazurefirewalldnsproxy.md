#### Parser Content
```Java
{
Name = microsoft-azuremon-sk4-dns-success-azurefirewalldnsproxy
  ParserVersion = "v1.0.0"
  Conditions = [ """"category":"AzureFirewallDnsProxy"""", """"resourceId":"""" ]
  Fields = ${LMSMSParsersTemplates.azure-ad-activity-2.Fields}[
    """"category":"({category}AzureFirewallDnsProxy)""",
    """"RuleCollection":"({rule_type}[^"]+)""""
    """"RuleCollectionGroup":"({rule_source}[^"]+)""""
   ]


}
```