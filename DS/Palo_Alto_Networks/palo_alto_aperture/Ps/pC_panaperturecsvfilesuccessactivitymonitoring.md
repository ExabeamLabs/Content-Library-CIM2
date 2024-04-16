#### Parser Content
```Java
{
Name = "pan-aperture-csv-file-success-activitymonitoring"
Vendor = "Palo Alto Networks"
Product = "Palo Alto Aperture"
TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
Conditions = [
"""activity_monitoring"""
""" Aperture """
""",file,"""
]
Fields = [
"""({time}\d+-\d+-\d+T\d+:\d+:\d+\.\d+Z)\s({host}[^\s]+)"""
"""activity_monitoring,"?({app}[^,"]+)"""
""","*\s*({file_name}[^,"]+?(\.\s*({file_ext}[^\.",]+?))?)"*,file"""
"""activity_monitoring,"*([^,]*,){5}({src_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3}),"""
""",file,"*([\w\s]+|({email_address}[^@]+@[^",]+))"*,({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
""",({access}[^,]+),(|[^,]),file"""
""",file,"*([\w\s]+|([^@]+@[^",]+))"*,([A-Fa-f.\d:]+),\w+,({access}[\w]+)"*,"""
""",file,"*([\w\s]+|([^@]+@[^",]+))"*,([A-Fa-f.\d:]+),"+[^"]+"+,({access}[\w]+)"*,""",
"""((?:1969-[^,]+?)|({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d+[\+-]\d+:\d+))"""
]
ParserVersion = "v1.0.0"


}
```