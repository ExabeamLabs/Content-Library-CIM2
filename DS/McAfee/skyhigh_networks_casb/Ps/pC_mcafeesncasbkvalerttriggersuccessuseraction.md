#### Parser Content
```Java
{
Name = "mcafee-sncasb-kv-alert-trigger-success-useraction"
Vendor = "McAfee"
Product = "Skyhigh Networks CASB"
TimeFormat = "MMM dd yyyy HH:mm:ss.SSS"
Conditions = [
""" activityName ="""
"""MimeType,"""
""",userAction="""
]
Fields = [
""",updatedOn=\"({time}\w+ \d+ \d\d\d\d \d\d:\d\d:\d\d\.\d+)"""
"""\d\d:\d\d:\d\d ({host}[^\s]+) activityName ="""
""",riskSeverity=({alert_severity}[^,]+)"""
""",activityName =({alert_name}[^,]+)"""
""",userAction=({alert_name}[^,]+)"""
""",destinationHost=({dest_host}[^,]+)"""
""",userDisplayName =({user}[^,\s]+)"""
""",incidentId=({alert_id}[^,]+)"""
""",response=({action}[^,]+)"""
""",riskScore=({original_risk_score}\d+)"""
""",serviceNames=\[({service_name}[^,\]]+)"""
]
DupFields = [
"alert_name->alert_type"
]
ParserVersion = "v1.0.0"


}
```