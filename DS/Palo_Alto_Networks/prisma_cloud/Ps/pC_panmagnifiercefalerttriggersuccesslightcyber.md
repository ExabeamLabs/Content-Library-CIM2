#### Parser Content
```Java
{
Name = "pan-magnifier-cef-alert-trigger-success-lightcyber"
  Vendor = "Palo Alto Networks"
  Product = "Prisma Cloud"
  TimeFormat = ["yyyy-MM-dd'T'HH:mm:ss.SSSZ", "yyyy-MM-dd HH:mm:ss"]
  Conditions = [
  """|LightCyber|Magna|"""
  ]
  Fields = [
  """start=({time}\d\d\d\d-\d\d-\d\d \d\d:\d\d:\d\d)"""
  """\|LightCyber\|Magna\|[^|]+?\|[^|]+?\|({alert_name}[^|]+?)\|"""
  """\|LightCyber\|Magna\|[^|]+?\|[^|]+?\|[^|]+?\|({alert_severity}[^|]+?)\|"""
  """\sexternalId=({alert_id}\d+)"""
  """\sshost=(?: |({src_host}.+?))\s*\w+="""
  """\ssuser=(?: |({user}[\w\.\-\!\#\^\~]{1,40}\$?))\s*\w+="""
  """\ssrc=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
  """\scs1=(?: |({alert_type}.+?))\s*\w+="""
  """\smsg=(?: |({additional_info}.+?))\s*\w+="""
  """\sfilePath=(?: |({malware_url}.+?))\s*\w+="""
  """\|LightCyber\|Magna\|[^|]+?\|[^|]+?\|({alert_type}[^|]+?)\|[^"]+?\s+cs2=({alert_name}[^=]+?)\s+fileHash=""",
  """((?:1969-[^,]+?)|({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d+[\+-]\d+:\d+))"""
  ]
  DupFields = [
  "malware_url->process_name"
  ]
  ParserVersion = "v1.0.0"


}
```