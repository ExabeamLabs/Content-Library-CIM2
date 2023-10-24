#### Parser Content
```Java
{
Name = vmware-carbonblackedr-kv-alert-trigger-ingresshit
  Vendor = VMware
  Product = Carbon Black EDR
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Conditions = [ """reason=feed.ingress.hit""", """host=""", """sensor_id=""" ]
  Fields = [
  """({time}\d\d\d\d-\d\d-\d\d \d\d:\d\d:\d\d)""",
  """reason=({alert_type}[^\s]+)""",
  """ioc_value='({additional_info}[^']+)'""",
  """feed_name='({alert_name}[^']+)""",
  """feed_id=({alert_id}\d+)""",
  """host='({dest_host}[^']+)""",
  """process_md5='({hash_md5}[^']+)""",
  """ioc_type='md5'\s+ioc_value='({hash_md5}[^']+)'""",
  """process_guid=({process_guid}[^\s]+)""",
  """sensor_id=({sensor_id}[^\s]+)""",
  """ioc_value='({ioc}.+?)'\s+\w+=""",
  ]
  ParserVersion = "v1.0.0"


}
```