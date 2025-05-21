#### Parser Content
```Java
{
Name = "vmware-carbonblackedr-kv-alert-trigger-success-watchlistid"
Vendor = "VMware"
Product = "Carbon Black EDR"
TimeFormat = "epoch_sec"
Conditions = [
  """reason=watchlist.hit"""
  """watchlist_name='"""
  """watchlist_id="""
  """process_guid="""
]
Fields = [
  """host='({host}[^']+)"""
  """timestamp='({time}\d{10})"""
  """interface_ip='(0.0.0.0|({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?)'"""
  """reason=({alert_type}[^\s]+)"""
  """watchlist_name='({alert_name}[^']+)'"""
  """process_md5='({hash_md5}[^']+)"""
  """process_guid=({process_guid}[^\s]+)"""
  """sensor_id=({sensor_id}[^\s]+)"""
  """process_path='({process_path}({process_dir}(?:[^=]+)?[\\\/])?({process_name}[^\\\/=]+))'\s+\w+="""
  """process_name='({process_name}[^']+)'"""
]
ParserVersion = "v1.0.0"


}
```