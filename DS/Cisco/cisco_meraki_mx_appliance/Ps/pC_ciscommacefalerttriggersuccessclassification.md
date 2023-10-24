#### Parser Content
```Java
{
Name = "cisco-mma-cef-alert-trigger-success-classification"
Vendor = "Cisco"
Product = "Cisco Meraki MX appliance"
TimeFormat = ["epoch_sec","yyyy-MM-dd'T'HH:mm:ss.SSSSSSZ"]
Conditions = [
  """destinationServiceName =Cisco Meraki"""
  """security_events"""
  """"classification":"""
  """"signature":"""
]
Fields = [
  """\WdestinationServiceName =(|({event_subtype}.+?))(\s+\w+=|\s*$)"""
  """\Wdproc=(|({process_path}[^=]+?))(\s+\w+=|\s*$)"""
  """"destIp":"({dest_ip}\d{1,3}.\d{1,3}.\d{1,3}.\d{1,3}):({dest_port}\d+)""""
  """"ts":"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d(\.\d+)?Z)"""",
  """"ts":({time}\d{10})"""
  """"srcIp":\"({src_ip}\d{1,3}.\d{1,3}.\d{1,3}.\d{1,3}):({src_port}\d+)""""
  """"protocol":\"({protocol}[^\"]+)""""
  """"blocked":({result}\w+),"""
  """"message":"({alert_name}[^\"]+)""""
  """"deviceMac":"({src_mac}[^\"]+)""""
  """"priority":"({alert_severity}\d+)""""
  """destinationServiceName =({app}Cisco Meraki)"""
  """"eventType":"({alert_type}[^"]+)""""
]
ParserVersion = "v1.0.0"


}
```