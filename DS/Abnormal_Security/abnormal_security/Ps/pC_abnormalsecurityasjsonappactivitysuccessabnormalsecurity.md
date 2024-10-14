#### Parser Content
```Java
{
Name = "abnormalsecurity-as-json-app-activity-success-abnormalsecurity"
ExtractionType = json
ParserVersion = "v1.0.0"
Vendor = "Abnormal Security"
Product = "Abnormal Security"
TimeFormat = "yyyy-MM-dd'T'HH:mm:ssZ"
Conditions = [ """destinationServiceName =Abnormal Security""", """dproc=cases""" , """"caseId":""" ,""""remediation_status":"""" ]
Fields = [
"""exa_json_path=$..customerVisibleTime,exa_field_name=time"""
"""exa_json_path=$..description,exa_field_name=description"""
"""exa_json_path=$..confidence,exa_field_name=alert_severity"""
"""exa_json_path=$..threatIds,exa_field_name=alert_id"""
"""exa_json_path=$..affectedEmployee,exa_field_name=full_name"""
"""exa_json_path=$..case_status,exa_field_name=result"""
"""exa_json_path=$..remediation_status,exa_field_name=additional_info"""
]


}
```