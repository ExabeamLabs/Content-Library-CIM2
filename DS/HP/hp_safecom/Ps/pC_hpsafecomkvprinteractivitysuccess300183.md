#### Parser Content
```Java
{
Name = hp-safecom-kv-printer-activity-success-300183
Vendor = "HP"
Product = "HP SafeCom"
TimeFormat = "yyyy-MM-dd HH:mm:ss"
Conditions = [
  """ JobName =""""
  """, JobDateTime=""""
]
Fields = [
  """\WPMComputerName ="({host}[\w\-.]+)"""
  """\WDocComputerName ="({host}[\w\-.]+)"""
  """\WJobDateTime="({time}\d\d\d\d\-\d\d\-\d\d \d\d:\d\d:\d\d)"""
  """\WJobName ="({object}[^",]+)"""
  """\WDeviceName ="({printer_name}[^",]+)"""
  """\WDeviceName ="({operation}[^",]+)"""
  """\WUserLogon="({user}[^\s",]+)"""
  """\WUserFullName ="({user}[^\s",]+)"""
  """\WUserEMail="({email_address}[^\s",]+)"""
  """\WJobSize="({bytes}\d+)"""
  """\WTrackingPageCount="({num_pages}\d+)"""
]
DupFields = [
  "host->dest_host"
]
ParserVersion = "v1.0.0"


}
```