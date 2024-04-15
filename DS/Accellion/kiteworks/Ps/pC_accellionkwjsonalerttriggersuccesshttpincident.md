#### Parser Content
```Java
{
Name = "accellion-kw-json-alert-trigger-success-httpincident"
Vendor = "Accellion"
Product = "Kiteworks"
TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
Conditions = [
"""subject=HTTP incident"""
""", incident-id="""
""", Sender Email="""
""", recipient-email1="""
]
Fields = [
""", incident-reported-on=({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d+(\+|\-)\d+)"""
"""policy-desc=({alert_name}[^,]+)"""
""", Employee Code=({user}[^,]+)"""
""", Sender Email=({email_address}[^,@]+@[^,@]+)"""
""", attachment-name1=({file_name}[^,]+)"""
""", attachment-size1=({bytes}\d+)"""
""", policy-name=({alert_type}[^,]+)"""
""", incident-id=({alert_id}[^,]+)"""
""", recipient-email1=({additional_info}[^,]+)"""
"""^.*?, First Name =({first_name}[^,]+)"""
"""^.*?, Last Name =({last_name}[^,]+)"""
""", protocol=({protocol}[^,]+)"""
""", incident-severity=({alert_severity}[^,]+)"""
""", monitor-host=({host}[^,]+)"""
""", recipient-url1=({malware_url}[^,]+)"""
""", mail_status=({action}[^,]+)"""
]
ParserVersion = "v1.0.0"


}
```