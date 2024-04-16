#### Parser Content
```Java
{
Name = microsoft-nsgflowlogs-sk4-network-traffic-success-nsgflowvents
  ParserVersion = v1.0.0
  Vendor = Microsoft
  Product = Network Security Group Flow Logs
  TimeFormat=["yyyy-MM-dd'T'HH:mm:ss.SSSZ", "yyyy-MM-dd'T'HH:mm:ss.SSSSSSSZ"]
  Conditions=[ """requestClientApplication=NSG Flow logs""", """"operationName":"NetworkSecurityGroupFlowEvents""""]
  Fields=[
		"""\"time\":\"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)"""
    """\"time\":\"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d(\.\d{1,7})?Z)"""
		"""\Wsuser=(anonymous|({email_address}([A-Za-z0-9]+[!#$%&'+-\/=?^_`~])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)|({user}[\w\.\-]{1,40}\$?))(\s+|\s*$)"""
		"""destinationServiceName =({app}[^=]+)\s+(\w+=|$)"""
		"""\WrequestClientApplication=(|({app}.+?))(\s+\w+=|\s*$)"""	
		"""category\":\"({operation}[^"]+)"""
		""""operationName":"({operation}[^"]+)""""
		"""rule":"({rule}[^"\\]+)"""
		"""\Wdproc=({event_name}({category}[^,;\=]+)[^\=]*?)\s+(\w+=|$)"""
		""""mac":\s*"({src_mac}[^"]+)"""
    """"category":"({category}[^,]+)""""
    """resourceId":"[^"]*\/RESOURCEGROUPS\/({resource_group}[^\/]+)\/"""
    """"operationName":"({event_name}[^,]+)""""
    """"resourceId":"[^"]*\/NETWORKSECURITYGROUPS\/({security_group}[^"]+)"""
  ]


}
```