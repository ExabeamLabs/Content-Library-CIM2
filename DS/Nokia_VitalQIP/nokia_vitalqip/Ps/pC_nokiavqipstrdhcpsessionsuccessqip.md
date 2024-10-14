#### Parser Content
```Java
{
Name = "nokia-vqip-str-dhcp-session-success-qip"
Vendor = "Nokia VitalQIP"
Product = "Nokia VitalQIP"
TimeFormat = ["dd/MM/yyyy HH:mm:ss", "MM/dd/yyyy HH:mm:ss"]
Conditions = [
  """QIP[-]: """
]
Fields = [
  """QIP\[\-\]:([^,]*,){6}\s*({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?"""
  """QIP\[\-\]:([^,]*,){7}\s*({dest_host}[^,]*?)\s*,"""
  """QIP\[\-\]:([^,]*,){8}\s*({domain}([^,\s]{1,256}\s*?){1,256}?)\s*,"""
  """QIP\[\-\]:([^,]*,){10}\s*({user}[\w\.\-\!\#\^\~]{1,40}\$?)\s*,"""
  """QIP\[\-\]:([^,]*,){11}\s*({time}\d\d\/\d\d\/\d\d\d\d \d\d:\d\d:\d\d)"""
]
ParserVersion = "v1.0.0"


}
```