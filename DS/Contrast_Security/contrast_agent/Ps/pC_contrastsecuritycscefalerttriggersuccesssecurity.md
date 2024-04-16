#### Parser Content
```Java
{
Name = "contrastsecurity-cs-cef-alert-trigger-success-security"
Vendor = "Contrast Security"
Product = "Contrast Agent"
TimeFormat = "MMM dd yyyy HH:mm:ss.SSS"
Conditions = [
"""CEF:"""
"""|Contrast Security|"""
"""|SECURITY|"""
]
Fields = [
"""({time}\w+ \d+ \d\d\d\d \d\d:\d\d:\d\d\.\d+)\s+({host}\S+)\s+CEF:([^\|]*\|){4}(|({alert_type}[^\|]+))\|(|({additional_info}[^\|]+))\|(|({alert_severity}[^\|]+))\|"""
"""\Wpri=(|({alert_name}.+?))(\s+\w+=|\s*$)"""
"""\Wsrc=(0:0:0:0:0:0:0:1|({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?)"""
"""\Wspt=(0|({src_port}\d+))"""
"""\Wrequest=(|({malware_url}.+?))(\s+\w+=|\s*$)"""
"""\Wapp=(|({process_name}.+?))(\s+\w+=|\s*$)"""
"""\Waction=(|({action}.+?))(\s+\w+=|\s*$)"""
]
ParserVersion = "v1.0.0"


}
```