#### Parser Content
```Java
{
Name = "servicenow-s-kv-app-activity-success-operation"
Vendor = "ServiceNow"
Product = "ServiceNow"
TimeFormat = "yyyy-MM-dd HH:mm:ss"
Conditions = [
""",sys_created_on=""""
""",dv_sys_class_name=""""
""",dv_number=""""
]
Fields = [
""",sys_created_on="({time}\d\d\d\d-\d\d-\d\d \d\d:\d\d:\d\d)"""
""",dv_sys_class_name="({operation}[^"]+)"""
""",dv_number="({object}[^"]+)"""
""",incident_state="({resource}[^"]+)"""
""",dv_assignment_group="({additional_info}[^"]+)"""
""",sys_created_by="({user}[\w\.\-]{1,40}\$?)"""
""",dv_assigned_to="(|({user}[\w\.\-]{1,40}\$?))"""
"""({app}ServiceNow)"""
]
ParserVersion = "v1.0.0"


}
```