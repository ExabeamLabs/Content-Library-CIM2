#### Parser Content
```Java
{
Name = "forcepoint-dlp-cef-email-receive-success-emaildelivery"
Vendor = "Forcepoint"
Product = "Forcepoint DLP"
TimeFormat = "epoch"
Conditions = [
  """CEF:"""
  """|Forcepoint|AP-EMAIL|"""
  """|Delivery|Delivery|"""
]
Fields = [
  """CEF:([^\|]*\|){6}({alert_severity}[^\|]+)"""
  """\Wrt=({time}\d{13})"""
  """\Wdvc=({host}[\d.]+)"""
  """\Wdvchost=({host}[\w\-.]+)"""
  """\Wsrc=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
  """\Wdst=({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?"""
  """\Wact=(|({result}\S+))\s"""
  """\WmessageId=({alert_id}\d+)"""
]
ParserVersion = "v1.0.0"


}
```