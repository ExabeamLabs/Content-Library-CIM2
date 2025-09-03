#### Parser Content
```Java
{
Name = microsoft-azuremon-sk4-http-request-success-azurefirewallapplicationrule
  ParserVersion = "v1.0.0"
  Conditions = [ """"category":"AzureFirewallApplicationRule"""", """"resourceId":"""", """Action: Deny""" ]
  Fields = ${LMSMSParsersTemplates.azure-ad-activity-2.Fields}[
    """"category":"({category}AzureFirewallApplicationRule)""",
    """"msg":"HTTPS?\s+request from\s({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?\s*to\s*(({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))|({web_domain}[\w\-\.]+))(:({dest_port}\d+))?""",
    """\sAction:\s*({action}Deny)"""
   ]


}
```