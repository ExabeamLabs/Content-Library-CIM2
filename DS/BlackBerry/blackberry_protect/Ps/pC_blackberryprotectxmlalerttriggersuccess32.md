#### Parser Content
```Java
{
Name = "blackberry-protect-xml-alert-trigger-success-32"
Vendor = "BlackBerry"
Product = "BlackBerry Protect"
TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSSSSSSSZ"
Conditions = [
"""<Event xmlns="""
"""<Provider Name ='CylanceSvc'"""
""">32</EventID>"""
]
Fields = [
"""<TimeCreated SystemTime='({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d+Z)"""
"""<Computer>({host}.+?)<\/Computer>"""
"""({alert_type}A potentially malicious Active script was Detected)"""
"""Device:\s*({src_host}[\w\-.]+)"""
"""MAC:\s*({src_mac}[^\s,;<]+)"""
"""File path:\s*(|({malware_url}.+?))\s+Process Id:"""
"""IP:\s({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
]
DupFields = [ "alert_type->alert_name" ]
ParserVersion = "v1.0.0"


}
```