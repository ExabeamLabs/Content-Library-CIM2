#### Parser Content
```Java
{
Name = "ordr-sce-json-alert-trigger-success-warning"
  Vendor = "Ordr"
  Product = "Ordr SCE"
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
  Conditions = [ """: WARNING [""", """] The device """, """) with severity level """, """"alarmCategory":""", """"severityLevel":""", """"alarmType":""" ]
  Fields = [
    """"timestamp":\s*"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)"""
    """"srcHost":\s*"([\d\w:]+|({host}[^"]+))""""
    """"severityLevel":\s*"({alert_severity}[^"]+)""""
    """"alarmCategory":\s*"({alert_type}[^"]+)""""
    """"alarmType":\s*"({alert_name}[^"]+)""""
	  """"alarmCategory":\s*"({alert_name}[^"]+)"""" 
    """"dstIp":\s*"({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?""""
    """"clientId":\s*"({dest_mac}[^"]+)""""
    """"dstPort":\s*({dest_port}\d+)"""
    """"srcPort":\s*({src_port}\d+)"""
    """"protocol":\s({protocol}\d+)"""
    """"srcIp":\s*"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""""
    """"srcMac":\s*"({src_mac}[^"]+)""""
    """"dstHost":\s*"({dest_host}[\w.-]+)""""
	  """"deviceType":\s*"({device_type}[^"]+)"""
	  """"mfgName":\s*"({additional_info}[^"]+)"""
	  """"modelNameNo":\s*"({device_model}[^"]+)"""
	  """"deviceGroup":\s*"({dest_group}[^"]+)"""
	  """"protocol":\s*({ip_protocol_id}\d+)\s*,"""
	  """"deviceName":\s*"({src_host}[\w.-]+)"""
  ]
  ParserVersion = "v1.0.0"
}  
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