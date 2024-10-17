#### Parser Content
```Java
{
Name = "symantec-endpointprotection-cef-alert-trigger-success-atpincident"
Vendor = "Symantec"
Product = "Symantec Endpoint Protection"
TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
Conditions = [
"""CEF:"""
"""|Symantec|"""
"""|atp_incident|"""
]
Fields = [
""""device_time":"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d+Z)"""
""""user_name":"({user}[\w\.\-\!\#\^\~]{1,40}\$?)"""
""""uuid":"({user_uid}[^"]+)"""
"""({host}[\w.\-]+)\s+atp_incident:"""
""""detection_type":"({alert_type}[^"]+)"""
"""rule_name=({alert_name}[^=]+?)\s\w+="""
"""description=({additional_info}[^=]+?)\s\w+="""
""""atp_incident_id":({alert_id}\d+)"""
""""incident_priority_level":"({alert_severity}[^"]+)"""
]
ParserVersion = "v1.0.0"


}
```