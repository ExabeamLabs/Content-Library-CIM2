#### Parser Content
```Java
{
Name = "mcafee-sncasb-kv-alert-trigger-success-hierarchy"
Vendor = "McAfee"
Product = "Skyhigh Networks CASB"
Conditions = [
""",riskLevel="""
""",policy_id="""
""",hierarchy="""
""",userDisplayName ="""
""",response="""
]
TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
Fields = [
""",created_on_date=({time}\d\d\d\d\-\d\d\-\d\dT\d\d:\d\d:\d\d\.\d\d\dZ)"""
"""\d\d:\d\d:\d\d\s+({host}[\w\-.]+)\s+(\w+=|$)"""
""",policy_name=({alert_name}[^,]+)"""
""",type=({alert_type}[^,]+)"""
""",riskLevel=({alert_severity}[^,]+)"""
""",hierarchy=({process_dir}[^,]+)"""
""",hierarchy=({target}[^,]+)"""
""",name=({file_name}[^,]+)"""
""",serviceName =({additional_info}[^,]+)"""
""",response=({action}[^,]+)"""
""",userDisplayName =({user}[^\s@,]+)"""
""",size=({bytes}\d+)"""
]
ParserVersion = "v1.0.0"


}
```