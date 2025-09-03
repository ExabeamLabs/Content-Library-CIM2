#### Parser Content
```Java
{
Name = microsoft-defenderep-json-alert-trigger-success-incidentname
  Vendor = Microsoft
  Product = Microsoft Defender
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSSSSSZ"
  ExtractionType = json
  Conditions = [ """"assignedTo":""", """"classification":""", """"determination":""", """"redirectIncidentId":""", """"severity":""", """"status":"""
 ]
  Fields = [
   """exa_json_path=$.incidentId,exa_field_name=alert_id"""
   """exa_json_path=$.incidentName,exa_field_name=event_name"""
   """exa_json_path=$.createdTime,exa_field_name=time"""
   """exa_json_path=$.status,exa_field_name=incident_status"""
   """exa_json_path=$.severity,exa_field_name=alert_severity"""
   """exa_json_path=$.incidentUri,exa_field_name=additional_info"""
   """exa_json_path=$.createdDateTime,exa_field_name=time"""
   """exa_json_path=$.description,exa_field_name=description"""
   """exa_json_path=$.determination,exa_field_name=result"""
   """exa_json_path=$.displayName,exa_field_name=event_name"""
   """exa_json_path=$.id,exa_field_name=alert_id"""
   """exa_json_path=$.incidentWebUrl,exa_field_name=additional_info"""
  ]
   ParserVersion = v1.0.0


}
```