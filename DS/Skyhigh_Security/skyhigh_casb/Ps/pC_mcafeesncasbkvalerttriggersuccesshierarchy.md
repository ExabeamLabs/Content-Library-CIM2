#### Parser Content
```Java
{
Name = "mcafee-sncasb-kv-alert-trigger-success-hierarchy"
Vendor = "Skyhigh Security"
Product = "Skyhigh CASB"
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
""",userDisplayName =({user}[\w\.\-\!\#\^\~]{1,40}\$?)"""
""",size=({bytes}\d+)"""
]
ParserVersion = "v1.0.0"


}
```