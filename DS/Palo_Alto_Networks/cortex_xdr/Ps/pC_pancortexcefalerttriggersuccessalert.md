#### Parser Content
```Java
{
Name = "pan-cortex-cef-alert-trigger-success-alert"
  Vendor = "Palo Alto Networks"
  Product = "Cortex XDR"
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
  Conditions = [
    """Palo Alto Networks|Cortex XDR"""
    """|Alert|"""
  ]
  Fields = [
    """({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)"""
    """CEF:[^|]+?\|([^\|]+\|){4}({alert_name}[^\|]+)"""
    """\WexternalId=({alert_id}.+?)\s+"""
    """\Wcat=({alert_type}.*?)\s+"""
    """\Wcs2=({process_path}.*?)\s*cs2Label"""
    """\Wcs1=({process_name}.*?)\s+"""
    """fileHash=({hash_sha256}[A-Za-z0-9]+)\s"""
    """\Wcs2=\"({process_dir}.*?)\"\s+"""
    """\Wshost=(({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))|({src_host}.*?))\s+"""
    """\Wsuser=(N/A|(({domain}[^\\]+)\\+)?({user}[\w\.\-]{1,40}\$?))(\s+\w+=|\s*$)"""
    """\Wrequest=({additional_info}.*?)\s+""",
    """((?:1969-[^,]+?)|({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d+[\+-]\d+:\d+))"""
  ]
  DupFields = [
    "process_path->path"
  ]
  ParserVersion = "v1.0.0"


}
```