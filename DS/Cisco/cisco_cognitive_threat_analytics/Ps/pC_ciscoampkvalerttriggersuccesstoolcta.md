#### Parser Content
```Java
{
Name = cisco-amp-kv-alert-trigger-success-toolcta
Vendor = "Cisco"
Product = "Cisco Cognitive Threat Analytics"
TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSS"
Conditions = [
  """ tool=cta:tool-cta """
  """ incidentTitle="""
  """ cIP="""
]
Fields = [
  """({time}\d{4}-\d{2}-\d{2}T\d{2}:\d{2}:\d{2}\.\d{1,3})Z\s+customer="""
  """({host}cta)"""
  """\sincidentId=({alert_id}\S+)"""
  """\sincidentTitle=({alert_name}\S.+?)\s+(\w+=|$)"""
  """\srisk=({alert_severity}\d+)"""
  """\sriskCategory=({alert_severity}\S.+?)\s+(\w+=|$)"""
  """\scIP=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
  """\ssIP=({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?"""
  """\scsUrl=({malware_url}\S+)"""
  """\scUsername=({user}[\w\.\-]{1,40}\$?)\s+(\w+=|$)"""
  """\sactivity=({additional_info}\S.+?)\s+(\w+=|$)"""
]
DupFields = [
  "alert_name->alert_type"
]
ParserVersion = "v1.0.0"


}
```