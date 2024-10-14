#### Parser Content
```Java
{
Name = "imperva-counterbreach-cef-alert-trigger-success-accessedtables"
Vendor = "Imperva"
Product = "CounterBreach"
TimeFormat = "yyyy-MM-dd HH:mm:ss"
Conditions = [
  """|Imperva Inc.|CounterBreach|"""
  """=AccessedTables"""
]
Fields = [
  """start=({time}\d+)"""
  """start=({time}\d{4}\-\d\d\-\d\d \d\d:\d\d:\d\d)"""
  """({host}[\w\-.]+) CEF:"""
  """\sdvc=({host}\d+\.\d+\.\d+\.\d+)"""
  """\sdvchost=({host}[\w\-.]+)"""
  """\scs2=\[?(({domain}[^\\=]+)\\+)?({db_user}[^\],\s]+)"""
  """\Wsuser=\[?({user}[\w\.\-\!\#\^\~]{1,40}\$?)"""
  """\Wshost=\[?({src_host}[\w\-.]+)"""
  """\scs4=\{applicativeTables:\[({table_name}[^\],]+)"""
  """\ssrc=\[?({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
  """\sdst=\[?({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?"""
  """CounterBreach\|([^|]+\|){2}({alert_name}[^|]+)"""
  """\smsg=({additional_info}.+?)\s\w+="""
  """\scat=({alert_type}.+?)\s\w+="""
  """CounterBreach\|([^|]+\|){3}({alert_severity}[^|]+)"""
  """\scs3=(\[\\*)?(?:|({db_object}.+?))\]?\s*\w+="""
  """|File\|.+?\scs3=(\[\\*)?([^\\]+\\+)*(?: |({file_name}.+?))\]?\s*\w+="""
  """\sact=(?:|({result}.+?))\s\w+="""
  """\scs5=({response_size}\d+)"""
  """\sdhost=({dest_host}[^\s]+)"""
]
DupFields = [
  "db_user->account"
]
ParserVersion = "v1.0.0"


}
```