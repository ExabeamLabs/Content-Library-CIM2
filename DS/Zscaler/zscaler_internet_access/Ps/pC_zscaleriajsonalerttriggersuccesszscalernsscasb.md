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
""""login":"""
""""recordid":"""
""""company":"""
]
Fields = [
""""dlpdictnames\":\"((None)|({alert_name}[^\"]+))\"\s*"""
""""dlpdictnames\":\"((None)|({dlp_dict}[^\"]+))\"\s*"""
""""dept\":\"({department}[^\"]+)\"\s*"""
""""applicationname\":\"({app}[^\"]+)\"\s*"""
""""Attachedfilename\":\"((None)|({file_name}[^\"]+))\"\s*"""
""""login\":\"({email_address}[^@]+@[^.]+\.[^\"]+)\"\s*"""
""""policy\":\"((None)|({policy_name}[^\"]+))\"\s*"""
]
DupFields = [
"alert_name->alert_type"
]
ParserVersion = "v1.0.0"


}
```