#### Parser Content
```Java
{
Name = microsoft-azuremon-sk4-http-request-success-azurefirewallapplicationrule
  ParserVersion = "v1.0.0"
  Conditions = [ """destinationServiceName =Azure""", """"category":"AzureFirewallApplicationRule"""", """"resourceId":"""", """dproc=EventHub""" ]
  Fields = ${LMSMSParsersTemplates.azure-ad-activity-2.Fields}[
    """"category":"({category}AzureFirewallApplicationRule)""",
   ]


}
```