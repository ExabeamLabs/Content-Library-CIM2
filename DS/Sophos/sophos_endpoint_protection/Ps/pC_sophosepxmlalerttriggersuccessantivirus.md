#### Parser Content
```Java
{
Name = sophos-ep-xml-alert-trigger-success-antivirus
Vendor = "Sophos"
Product = "Sophos Endpoint Protection"
TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSS"
Conditions = [
"""<Provider Name ='Sophos Anti-Virus'/>"""
"""<EventData><Data>"""
]
Fields = [
"""<TimeCreated SystemTime='({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d{3})"""
"""<Computer>({src_host}.+?)</Computer>"""
"""<EventData><Data>({alert_name}.+?)</Data><Data>({file_path}({file_dir}[^<>]+?)?({file_name}[^<>\\\/]*?(\.({file_ext}\w+))?))(\\\w+)?</Data><Data>.*?</Data><Data>({alert_type}.+?)</Data><Data>.*?</Data><Data>({result}.+?)\.?\s*</Data>"""
"""<Computer>({src_host}.+?)</Computer>"""
"""C:\\Users\\({user}[\w\.\-\!\#\^\~]{1,40}\$?)"""
"""</Message><Level>({alert_severity}[^\<]+)"""
]
ParserVersion = "v1.0.0"


}
```