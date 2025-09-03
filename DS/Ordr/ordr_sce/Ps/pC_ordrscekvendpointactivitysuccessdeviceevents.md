#### Parser Content
```Java
{
Name = "ordr-sce-kv-endpoint-activity-success-deviceevents"
  Vendor = "Ordr"
  Product = "Ordr SCE"
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Conditions = [ """"deviceType":""", """"eventType":""", """deviceEvents: INFO""", """ The device """ ]
  Fields = [
    """deviceEvents\s+({time}\d\d\d\d-\d\d-\d\d\s+\d\d:\d\d:\d\d),\d\d\d\s+"""
	  """"deviceId":\s*"({dest_mac}[^"]+)"""
  	""""osType":\s*"({os}[^"]+)"""
  	""""deviceType":\s*"({device_type}[^"]+)"""
	  """"osVersion":\s*"({os_version}[^"]+)"""
	  """"ipAddress":\s*\["({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?""""
	  """"eventType":\s*"({event_name}[^"]+)"""
	  """"riskState":\s*"({severity}[^"]+)"""
	  """"groupList":\s*({dest_group}\[[^\]\{]+\])"""
	  """"manufacturer":\s*"({additional_info}[^"]+)"""
  	""""modelNameNo":\s*"({device_model}[^"]+)"""
	  """"fqdn":\s*"({dest_host}[\w.-]+)"""
	  """"deviceDescr":\s*"({device_description}[^"]+)"""
	  """"subnet":\s*"({subnetwork}[^"]+)"""
  ]
  ParserVersion = "v1.0.0"


}
```