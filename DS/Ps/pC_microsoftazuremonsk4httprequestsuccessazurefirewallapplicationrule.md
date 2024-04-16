#### Parser Content
```Java
{
Name = microsoft-azuremon-sk4-http-request-success-azurefirewallapplicationrule
  ParserVersion = "v1.0.0"
  Conditions = [ """"category":"AzureFirewallApplicationRule"""", """"resourceId":"""", """Action: Deny""" ]
  Fields = ${LMSMSParsersTemplates.azure-ad-activity-2.Fields}[
    """"category":"({category}AzureFirewallApplicationRule)""",
   ]


}
```