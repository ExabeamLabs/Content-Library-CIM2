#### Parser Content
```Java
{
Name = microsoft-sentinel-sk4-alert-trigger-success-loganalyticscr
  ParserVersion = v1.0.0
  Vendor = Microsoft
  Product = Microsoft Sentinel
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSSSSSZ"
  Conditions = [ """"productName":"Azure Sentinel"""", """"vendorName":"Microsoft"""", """"severity":"""", """"kind":"SecurityAlert"""" ]
  Fields=[
  """"timeGenerated":"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d.\d\d\d\d\d\d\dZ)""",
	""""severity":"({alert_severity}[^"]+)""""
	"""properties":\{"title":"({alert_name}[^"]+?)(\\u200b)?""""
	"""incidentUrl":({malware_url}[^"]+)"""
	""""Query"*:"({additional_info}.+?)",""""
	""""Analytic Rule Name":"({rule}[^"]+)""",
	"""relatedEntities.+?"kind":"Account","properties":\s*\{.+?"friendlyName":"({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))"""
	""""kind":"Ip","properties":\{"address":"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
	""""workspaceInfo":.+?"ResourceGroupName":"({resource_group}[^"]+)"""
	""""workspaceInfo":.+?"SubscriptionId":"({subscription_id}[^"]+)"""
  """"alertType":"({alert_type}[^"]+)""""
    ]


}
```