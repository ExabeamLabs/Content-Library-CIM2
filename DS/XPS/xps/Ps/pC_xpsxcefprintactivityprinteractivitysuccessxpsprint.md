#### Parser Content
```Java
{
Name = "xps-x-cef-print-activity-printer-activity-success-xpsprint"
  Vendor = "XPS"
  Product = "XPS"
  TimeFormat = "yyyy-MM-dd HH:mm:ss a"
  Conditions = [
    """ XPS """
    """ PRINT"""
  ]
  Fields = [
    """({time}\d+\-\d+\-\d+\s+\d+:\d+:\d+ (PM|pm|AM|am))\s+({host}[^\s]+)\s+(?:-|({printer_name}[^\s]+))\s+\d+\s+(?:-|({user}[\w\.\-\!\#\^\~]{1,40}\$?))\s+[^\s]+\s+(?:-|({src_host}[^\s]+))\s+(?:-|({object}.+?))\s(\d*\s*){3}\d+\.\d+\s+.+?\s+(\d+\s+){3}XPS\s+({operation}PRINT)""" 
    """PRINTER=({printer_name}[^\s]+)"""
 ]
  DupFields = [
    "printer_name->dest_host"
  ]
  ParserVersion = "v1.0.0"


}
```