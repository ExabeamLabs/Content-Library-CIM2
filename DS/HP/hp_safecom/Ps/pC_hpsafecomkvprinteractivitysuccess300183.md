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
  """\WUserLogon="({user}[\w\.\-\!\#\^\~]{1,40}\$?)"""
  """\WUserFullName ="({user}[\w\.\-\!\#\^\~]{1,40}\$?)"""
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