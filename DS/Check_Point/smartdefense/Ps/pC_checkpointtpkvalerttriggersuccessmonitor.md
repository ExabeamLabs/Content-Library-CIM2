#### Parser Content
```Java
{
Name = "checkpoint-tp-kv-alert-trigger-success-monitor"
Vendor = "Check Point"
Product = "SmartDefense"
TimeFormat = "ddMMMyyyy HH:mm:ss"
Conditions = [
"""product: SmartDefense;"""
""" monitor """
]
Fields = [
"""\s({time}\d{2}\w{3}\d{4} \d\d:\d\d:\d\d)\s+\S+\s+\S+\s+product: SmartDefense;"""
"""\s({host}[\w\-\.]+)\s+product: SmartDefense;"""
"""\Wsrc:\s*({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?;"""
"""\Ws_port:\s*({src_port}\d+);"""
"""\Wdst:\s*({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?;"""
"""\Wservice:\s*({dest_port}\d+);"""
"""\Wproto:\s*(|({protocol}.+?));"""
"""\WSeverity:\s*(|({alert_severity}.+?));"""
"""\WProtection Name:\s*(|({alert_name}.+?));"""
"""\WAttack Info:\s*(|({alert_type}.+?));"""
"""\WProtection Type:\s*(|({additional_info}.+?));"""
]
ParserVersion = "v1.0.0"


}
```