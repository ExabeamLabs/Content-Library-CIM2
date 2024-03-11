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
  """\sPrinterIPAddress="({dest_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?"""
  """\sPrintFrom="({src_host}[^"]+)"""
  """\sIPAddress="({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
  """\sAlertType="({alert_type}[^"]+)"""
]
ParserVersion = "v1.0.0"


}
```