#### Parser Content
```Java
{
Name = microsoft-azuremon-sk4-alert-trigger-success-graphsecurityalerts
Vendor = Microsoft
Product = Azure Monitor
TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
Conditions = [
  """dproc=Graph Security Alerts"""
  """"provider":"Azure Sentinel""""
  """destinationServiceName =Azure"""
  """"alertDetections":"""
]
Fields = [
  """"eventDateTime":"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)"""
  """"title":"({alert_type}({alert_name}[^"]+?))(\\u200b)?""""
  """"severity":"({alert_severity}[^"]+)""""
  """"description":"({additional_info}[^"]+)""""
  """"userPrincipalName":"(null|({email_address}([A-Za-z0-9]+[!#$%&'+-\/=?^_`~])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)|({domain}[^\\\s"]+)\\+({user}[\w\.\-\!\#\^\~]{1,40}\$?))""""
  """"accountName":"({domain}[^\\\s"]+)\\+({user}[\w\.\-\!\#\^\~]{1,40}\$?)""""
  """"domainName":"({domain}[^"]+)""""
  """"id":"({alert_id}[^"]+)""""
  """\srequestClientApplication=({app}[^=]+)\s+\w+="""
]
ParserVersion = "v1.0.0"


}
```