#### Parser Content
```Java
{
Name = "ordr-sce-json-alert-trigger-success-warning"
Vendor = "Ordr"
Product = "Ordr SCE"
TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
Conditions = [
""": WARNING ["""
"""] The device ("""
""") with severity level """
""""dstIp":"""
""""peerId":"""
]
Fields = [
""""timestamp":\s*"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)"""
""""srcHost": "([\d\w:]+|({host}[^"]+))""""
""""severityLevel":\s"({alert_severity}[^"]+)""""
""""alarmHash":\s"({hash_md5}[^"]+)""""
""""alarmType":\s"({alert_name}[^"]+)""""
""""alarmCategory":\s"({alert_type}[^"]+)""""
""""dstIp":\s"({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?""""
""""clientId":\s"({dest_mac}[^"]+)""""
""""dstPort":\s*({dest_port}\d+)"""
""""srcPort":\s*({src_port}\d+)"""
""""protocol":\s({protocol}\d+)"""
""""srcIp":\s"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""""
""""srcMac":\s"({src_mac}[^"]+)""""
]
ParserVersion = "v1.0.0"


}
```