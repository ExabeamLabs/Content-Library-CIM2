#### Parser Content
```Java
{
Name = "cisco-cloudlock-json-alert-trigger-success-entityowneremail"
Vendor = "Cisco"
Product = "Cisco CloudLock"
TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
Conditions = [
""""entity_vendor_name":"""
""""entity_owner_email":"""
""""ctx_after":"""
]
Fields = [
""""created_at":\s*\"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)"""
""""id":\s*({alert_id}[^,]+)"""
""""policy_name":\s*\"({alert_name}[^\"]+)\""""
""""entity_origin_type":\s*\"({alert_type}[^\"]+)\""""
""""severity":\s*\"({alert_severity}[^\"]+)\""""
""""entity_name":\s*\"({target}[^\"]+)\""""
""""entity_owner_name":\s*\"({full_name}[^\"]+)\""""
""""entity_owner_email":\s*\"({email_address}[^\"]+)\""""
""""entity_vendor_name":\s*\"({process_path}[^\"]+)\""""
""""entity_direct_url":\s*\"({url}[^\"]+([^\\\/:\s.]+))\""""
""""entity_direct_url":\s*\"({additional_info}[^\"]+)\""""
]
ParserVersion = "v1.0.0"


}
```