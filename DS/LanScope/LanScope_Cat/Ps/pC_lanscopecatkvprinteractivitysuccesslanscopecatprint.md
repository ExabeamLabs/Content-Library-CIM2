#### Parser Content
```Java
{
Name = lanscope-cat-kv-printer-activity-success-lanscopecatprint
Vendor = "LanScope"
Product = "LanScope Cat"
TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
Conditions = [
  """LanScopeCat - Print"""
  """Printer="""
]
Fields = [
  """({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d+(\+|\-)\d\d:\d\d)\s+({host}\S+)\s+LanScopeCat\s+\-"""
  """\sEvent="({operation}[^"]+)"""
  """\sAgent="({dest_host}[^"]+)"""
  """\sLogonUser="({user}[^"]+)"""
  """\sPrinter="({printer_name}[^"]+)"""
  """\sDocument="({object}[^"]+)"""
  """\sNumOfPrintedPages="({num_pages}\d+)"""
  """\sPrinterIPAddress="({dest_ip}[^"]+)"""
  """\sPrintFrom="({src_host}[^"]+)"""
  """\sIPAddress="({src_ip}[a-fA-F\d.:]+)"""
  """\sAlertType="({alert_type}[^"]+)"""
]
ParserVersion = "v1.0.0"


}
```