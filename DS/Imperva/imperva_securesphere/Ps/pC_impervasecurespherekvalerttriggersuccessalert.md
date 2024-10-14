#### Parser Content
```Java
{
Name = "imperva-securesphere-kv-alert-trigger-success-alert"
Vendor = "Imperva"
Product = "Imperva SecureSphere"
TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
Conditions = [
  """ Imperva Inc.|SecureSphere,"""
  """cat=Alert"""
  """, Policy="""
]
Fields = [
  """\sduser=(?:n\/a|({db_user}[^,]+))"""
  """\sos-user=({user}[\w\.\-\!\#\^\~]{1,40}\$?)"""
  """\sApplicationName =(?: |({app}[^,]+))"""
  """\sServiceName =(?: |({service_name}[^,]+))"""
  """\sServerGroup=(?: |({server_group}[^,]+))"""
  """\sdatabase=(?: |({db_name}[^,]+))"""
  """\ssrc=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
  """\sdst=({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?"""
  """\salert=({alert_name}[^,]+)"""
  """,\sPolicy=({alert_type}[^,]+)"""
  """\ssev=({alert_severity}[^,]+)"""
  """\sDescription=({additional_info}.+?)\s+$"""
]
DupFields = [
  "db_user->account"
]
ParserVersion = "v1.0.0"


}
```