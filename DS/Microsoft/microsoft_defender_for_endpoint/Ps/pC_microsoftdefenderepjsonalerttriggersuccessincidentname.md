#### Parser Content
```Java
{
Name = microsoft-defenderep-json-alert-trigger-success-incidentname
  Vendor = Microsoft
  Product = Microsoft Defender for Endpoint
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSSSSSZ"
  Conditions = [ """"incidentUri":""", """"incidentName":""", """"status":""", """"incidentId":""" ]
  Fields = [
   """"incidentName":\s*"({event_name}[^"]+)"""",
   """"createdTime":\s*"({time}[^"]+)"""",
   """"status":\s*"({result}[^"]+)"""",
   """"severity":\s*"({alert_severity}[^"]+)"""",
   """"incidentUri":\s*"({additional_info}[^}\]]+?)\s*"[,\]}]""",
   ]
   ParserVersion = v1.0.0


}
```