#### Parser Content
```Java
{
Name = "dtexsystems-intercept-cef-printer-activity-success-dtex"
Vendor = "Dtex Systems"
Product = "DTEX InTERCEPT"
TimeFormat = "epoch"
Conditions = [
"""CEF:"""
"""|Dtex|"""
"""|PrintJobActivity|PrintJobIssued|"""
]
Fields = [
"""\Wstart=({time}\d{13})"""
"""\WDevice_Name =(({domain}[^\\]+)\\+)?({host}[^\\\s]+)"""
"""\WUser_Name =(({domain}[^\\]+)\\+)?({user}[\w\.\-\!\#\^\~]{1,40}\$?)\s"""
"""Printer_Details=\{.*?"Name":\s*"({printer_name}[^"\s]+)"""
"""Printer_Pages=({num_pages}\d+)"""
"""Source_File_Name =({object}.+?)\s*(\w+=|$)"""
"""reason=.+?\[({num_pages}\d+)\spage\(s\)\]\[({bytes}\d+)\sbytes"""
"""([^\|]*\|){5}({operation}[^\|]+)"""
]
DupFields = [
"host->src_host"
]
ParserVersion = "v1.0.0"


}
```