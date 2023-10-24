#### Parser Content
```Java
{
Name = "nexpose-insightvm-kv-alert-trigger-success-solutionsummary"
Vendor = "Rapid7"
Product = "Rapid7 InsightVM"
TimeFormat = "yyyy-MM-dd HH:mm:ss.SSS"
Conditions = [
""", solution_summary=""""
""", signature=""""
""", severity=""""
]
Fields = [
"""\Wdvc=\"({host}[\w.\-]+)"""
"""\Wtimestamp=\"({time}\d\d\d\d-\d\d-\d\d \d\d:\d\d:\d\d\.\d+)"""
"""\Wother_references=\"({additional_info}[^\"]+)\""""
"""\Wdest=\"(\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3}|({src_host}[^\"]+))\""""
"""\Wip=\"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
"""\Wseverity=\"({alert_severity}[^\"]+)\""""
"""\Wsignature=\"({alert_name}[^\"]+)\""""
"""\Wcategory=\"({alert_type}[^\"]+)\""""
]
DupFields = [
"host->dest_host"
]
ParserVersion = "v1.0.0"


}
```