#### Parser Content
```Java
{
Name = hp-printserver-kv-printer-activity-success-unspecified
Vendor = "HP"
Product = "Print Server"
TimeFormat = "yyyy-MM-dd HH:mm:ss.S"
Conditions = [
  """PRINTER_lab_LocalName =""""
  """PRINTER_lab_Type=""""
  """PRINTER_lab_SerialNumber=""""
]
Fields = [
  """JOB_date_Submitted="({time}\d+-\d+-\d+\s+\d+:\d+:\d+\.\d+)"""
  """MPS_lab_Name ="({host}[^"]+)"""
  """PRINTER_lab_LocalName ="(Unspecified|({printer_name}[^"]+))"""
  """PRINTER_lab_SerialNumber="(Unspecified|({printer_sn}[^"]+))"""
  """JOB_lab_NTUserName ="(Unspecified|({user}[^"]+))"""
  """Lab_NTFullUserName ="({last_name}[^",]+),\s*({first_name}[^",]+)"""
  """JOB_lab_NTUserMachine="(Unspecified|({src_host}[^"]+))"""
  """JOB_qty_PrintedPages="({num_pages}\d+)"""
  """JOB_lab_DocumentName ="(Unspecified|[\s-]*({object}[^"]+?))\s*""""
  """PRINTER_lab_Type="(Unspecified|({operation}[^"]+))"""
]
ParserVersion = "v1.0.0"


}
```