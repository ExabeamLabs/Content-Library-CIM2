#### Parser Content
```Java
{
Name = "symantec-dlp-cef-email-send-success-emailsend"
Vendor = "Symantec"
Product = "Symantec DLP"
TimeFormat = "yyyy-MM-dd HH:mm:ss"
Conditions = [
  """|Symantec|DLP|"""
  """|BLOCKED="""
  """INCIDENT_SNAPSHOT="""
]
Fields = [
  """\d\d:\d\d:\d\d\s+({host}[\w.\-]+)\s+CEF:"""
  """\|Symantec\|DLP\|[^|]*\|({alert_type}[^|]+)\|"""
  """\|Symantec\|DLP\|[^|]*\|({alert_name}[^|]+)\|"""
  """\sRULES=({alert_name}.+?)\s*(\w+=|$)"""
  """\|BLOCKED=(?:N\/A|None|({action}.+?))\s+(\w+=|$)"""
  """\sENDPOINT_MACHINE=(N\/A|({dest_host}[\w.\-]+))\s+(\w+=|$)"""
  """\sFILE_NAME=(?:N\/A|({file_name}.+?))\s+(\w+=|$)"""
  """\sINCIDENT_ID=({alert_id}\d+)"""
  """\sPROTOCOL=({protocol}.+?)\s+(\w+=|$)"""
  """\sSENDER=({src_email_address}[^@",]+?@[^"\.,]+?\.[^",\s]+?)\s+(\w+=|$)"""
  """\sRECIPIENTS=(?=[\w.]+@[\w.])({email_recipients}.+?)\s+(\w+=|$)"""
  """\sRECIPIENTS=(?=[\w.]+@[\w.])({external_address}[^,\s]+)"""
  """\sSEVERITY=({alert_severity}\d+:\w+)\s+"""
  """\sSUBJECT=(?:N\/A|({email_subject}.+?))\s+(\w+=|$)"""
  """\sUSER=(N\/A|(({domain}[^\\=]+)\\+)?({user}[\w\.\-]{1,40}\$?)\s+(\w+=|$))"""
  """\sDATAOWNER_NAME=(N\/A|(({domain}[^\\=]+)\\+)?({user}[\w\.\-]{1,40}\$?)\s+(\w+=|$))"""
  """\sINCIDENT_SNAPSHOT=\w+:\/+[^\s]*?((?!\d{1,3}\.\d{1,3}\.\d{1,3})({url}[^\s]+))\s+(\w+=|$)"""
  """\sENDPOINT_DEVICE_ID=(N\/A|({device_id}.+?))\s*(\w+=|$)"""
  """C:\\Users\\({user}[\w\.\-]{1,40}\$?)"""
]
DupFields = [
  "external_address->dest_email_address"
  "email_recipients->target"
  "email_subject->additional_info"
  "src_email_address->email_address"
]
ParserVersion = "v1.0.0"


}
```