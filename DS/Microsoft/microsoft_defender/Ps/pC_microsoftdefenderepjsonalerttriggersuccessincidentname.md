#### Parser Content
```Java
{
Name = microsoft-defenderep-json-alert-trigger-success-incidentname
  Vendor = Microsoft
  Product = Microsoft Defender
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSSSSSZ"
  ExtractionType = json
  Conditions = [ """"incidentUri":""", """"incidentName":""", """"status":""", """"incidentId":""" ]
  Fields = [
   """exa_json_path=$.incidentName,exa_field_name=event_name"""
   """exa_json_path=$.createdTime,exa_field_name=time"""
   """exa_json_path=$.status,exa_field_name=incident_status"""
   """exa_json_path=$.severity,exa_field_name=alert_severity"""
   """exa_json_path=$.incidentUri,exa_field_name=additional_info"""
   ]
   ParserVersion = v1.0.0


}
```