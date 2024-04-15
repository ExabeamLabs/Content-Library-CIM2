#### Parser Content
```Java
{
Name = "mcafee-dlp-cef-printer-activity-success-printername"
Vendor = "McAfee"
Product = "McAfee DLP Endpoint"
TimeFormat = "epoch"
Conditions = [
"""McAfee|Data Loss Prevention"""
"""|dlp """
"""cs2Label=Printer Name"""
]
Fields = [
"""(\s|\|)rt=({time}\d{13})\s+([\w\.-]+=|$)"""
"""(\s|\|)cs2=({printer_name}.+?)\s+([\w\.-]+=|$)"""
"""(\s|\|)shost=({src_host}.+?)\s+([\w\.-]+=|$)"""
"""(\s|\|)src=({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?\s+([\w\.-]+=|$)"""
"""(\s|\|)suser=({user}.+?)\s+([\w\.-]+=|$)"""
"""(\s|\|)sntdom=({domain}.+?)\s+([\w\.-]+=|$)"""
"""(\s|\|)fname=({object}.+?)\s+([\w\.-]+=|$)"""
"""(\s|\|)fsize=({bytes}\d+)\s+([\w\.-]+=|$)"""
"""(\s|\|)cs1=({additional_info}.+?)\s+([\w\.-]+=|$)"""
]
ParserVersion = "v1.0.0"


}
```