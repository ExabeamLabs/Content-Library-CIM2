#### Parser Content
```Java
{
Name = "hp-lprinter-json-printer-activity-success-laserjet"
Vendor = "HP"
Product = "HP LaserJet Printer"
TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
Conditions = [
"""LaserJet"""
"""job_lab_ntusername"""
]
Fields = [
"""@timestamp"+:"+({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d+Z)"""
"""host"+:"+({host}[^"]+)"""
"""job_lab_ntusername"+:"+(?:Unspecified|({user}[\w\.\-]{1,40}\$?))"""
"""job_lab_documentname"+:"+(?:Unspecified|({object}[^"]+))"""
"""job_qty_size"+:({bytes}\d+)"""
"""job_qty_printedpages"+:({num_pages}\d+)"""
"""printer_lab_localname"+:"+({printer_name}[^"]+)"""
"""printer_lab_ipaddress"+:["\s]*({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
"""port"*:({src_port}\d+)"""
"""job_lab_ntusermachine"+:"+(?:Unspecified|({src_host}[^"]+))"""
]
ParserVersion = "v1.0.0"


}
```