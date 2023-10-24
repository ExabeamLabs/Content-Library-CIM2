#### Parser Content
```Java
{
Name = "zscaler-ia-json-alert-trigger-success-zscalernsscasb"
Vendor = "Zscaler"
Product = "Zscaler Internet Access"
TimeFormat = "EEE MMM dd HH:mm:ss yyyy"
Conditions = [
""""zscalernss-casb""""
""""dlpenginenames":"""
""""recordid":"""
""""company":"""
]
Fields = [
""""threatname\":\"((None)|({alert_name}[^\"]+))\"\s*"""
""""dlpdictnames\":\"((None)|({dlp_dict}[^\"]+))\"\s*"""
""""dept\":\"({department}[^\"]+)\"\s*"""
""""applicationname\":\"({app}[^\"]+)\"\s*"""
""""Attachedfilename\":\"((None)|({file_name}[^\"]+))\"\s*"""
""""(login|owner)\":\"({email_address}[^@]+@[^.]+\.[^\"]+)\"\s*"""
""""policy\":\"((None)|({policy_name}[^\"]+))\"\s*""",
""""company":"({company}[^",]+)""",
""""bucket_name":"({bucket_name}[^",]+)""",
""""datetime":"({time}\w+ \w+ \d+ \d+:\d+:\d+ \d+)""",
""""tenant":"({tenant_id}[^",]+)""",
""""fullurl":"({url}[^",]+)""",
""""filesource":"({file_path}[^",]+)""",
""""filename":"({file_name}[^",]+)"""
]
DupFields = [
"alert_name->alert_type"
]
ParserVersion = "v1.0.0"


}
```