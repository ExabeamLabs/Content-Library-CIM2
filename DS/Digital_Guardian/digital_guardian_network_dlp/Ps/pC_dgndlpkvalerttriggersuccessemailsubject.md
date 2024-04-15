#### Parser Content
```Java
{
Name = "dg-ndlp-kv-alert-trigger-success-emailsubject"
Vendor = "Digital Guardian"
Product = "Digital Guardian Network DLP"
TimeFormat = "yyyy-MM-dd HH:mm:ss z"
Conditions = [
"""matched_policies_by_severity="""
"""email_subject="""

]
Fields = [
"""timestamp=\"({time}\d\d\d\d-\d\d-\d\d \d\d:\d\d:\d\d \w+)\""""
"""\d\d:\d\d ({host}[^\s]+)\s+\d+\s+\d{4}\-"""
"""source=\"(?:\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3}|({user}[^\"\\;]+))\""""
"""destination=\"(?:\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3}|({target}[^\"]+))\""""
"""inspected_document=\"(?:|({additional_info}.+?))\""""
"""protocol=\"({alert_type}[^\"]+)"""
"""protocol=\"({protocol}[^\"]+)"""
"""protocol=\"FTP\"\s+inspected_document=\"({file_name}[^\"]+)"""
"""action_taken=\"({action}[^\"]+)"""
"""source_ip=\"({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
"""destination_ip=\"({dest_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?"""
"""matched_policies_by_severity=\"*({alert_severity}[^\"]+)"""
"""matched_policies_by_severity=\"\w+:({alert_name}[^,;\/]+)"""
]
ParserVersion = "v1.0.0"


}
```