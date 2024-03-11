#### Parser Content
```Java
{
Name = microsoft-azuremon-sk4-dns-success-azurefirewalldnsproxy
  ParserVersion = "v1.0.0"
  Conditions = [ """destinationServiceName =Azure""", """"category":"AzureFirewallDnsProxy"""", """"resourceId":"""", """dproc=EventHub""" ]
  Fields = ${LMSMSParsersTemplates.azure-ad-activity-2.Fields}[
    """"category":"({category}AzureFirewallDnsProxy)""",
   ]


}
```