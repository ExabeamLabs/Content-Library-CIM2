#### Parser Content
```Java
{
Name = "pan-aperture-csv-alert-trigger-success-policyviolation"
Vendor = "Palo Alto Networks"
Product = "Palo Alto Aperture"
TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
Conditions = [
""" Aperture """
""",policy_violation,"""
]
Fields = [
"""({time}\d+-\d+-\d+T\d+:\d+:\d+\.\d+Z)\s({host}[^\s]+)"""
""",policy_violation,\"*({app}[^,\"]+)\"*,"""
""",policy_violation,\"*([^,]*,){1}({alert_severity}\d+(\.\d)?)"""
""",policy_violation,\"*([^,]*,){2}({alert_id}[^,]+)\"*,"""
""",policy_violation,\"*([^,]*,){4}\"*({email_address}[^@]+@[^,\"]+)\"*,([^,]*,){3}\"*({additional_info}[^\",]+)\s*\"*,"""
"""({alert_name}policy_violation)""",
"""((?:1969-[^,]+?)|({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d+[\+-]\d+:\d+))"""
]
DupFields = [
"alert_name->alert_type"
]
ParserVersion = "v1.0.0"


}
```