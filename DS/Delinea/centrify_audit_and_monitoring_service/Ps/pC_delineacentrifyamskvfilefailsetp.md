#### Parser Content
```Java
{
Name = "delinea-centrifyams-kv-file-fail-setp"
  Vendor = "Delinea"
  Product = "Centrify Audit and Monitoring Service"
  TimeFormat = "epoch"
  Conditions = [
   """Centrify Suite|"""
   """|SFTP"""
  ]
  Fields = [
    """utc=({time}\d{13})"""
    """user=({user}[^\(\)\s\$]+)"""
    """\d+\|\d+\|({event_name}.+?)\|\d"""
    """status=({result}.+?)\s\w+="""
    """pid=({process_id}\d+)"""
    """service=({protocol}.+?)\s\w+="""
    """operation=({operation}.+?)\s\w+="""
    """arguments=({file_path}({file_dir}.*?)(\/+({file_name}[^\/]+?))?)\s*(\w+=|$)"""
    """reason=({failure_reason}.+?)\s*$"""
  ]
  ParserVersion = "v1.0.0"


}
```