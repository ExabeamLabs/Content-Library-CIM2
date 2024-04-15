#### Parser Content
```Java
{
Name = "f5-asm-cef-alert-trigger-success-responsecode"
Vendor = "F5"
Product = "F5 Application Security Manager"
TimeFormat = "yyyy-MM-dd HH:mm:ss"
Conditions = [
  """ASM:"""
  """,web_application_name="""
  """,response_code="""
]
Fields = [
  """date_time="({time}\d\d\d\d-\d\d-\d\d \d\d:\d\d:\d\d)""""
  """\d\d:\d\d:\d\d ({dest_host}[^\s]+) ASM:"""
  """unit_hostname=\"({host}[^\"]+)""""
  """ip_client="({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""""
  """UserID=({user}[^\s,]+)"""
  """username=\"(N\/A|({user}[^\"]+))""""
  """src_port=\"({src_port}\d+)"""
  """dest_port=\"({dest_port}\d+)"""
  """dest_ip=\"({dest_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?"""
  """uri=\"(\/|({malware_url}[^\"]+?))\s*""""
  """policy_name=\"({policy_name}[^\"]+)""""
  """policy_name=\"({alert_name}[^\"]+)\""""
  """,violations=\"({alert_name}[^\"]+)\""""
  """violation_rating=\"({alert_severity}[^\"]+)""""
  """protocol=\"({protocol}[^\"]+)"""
  """protocol=\"({alert_type}[^\"]+)"""
  """,attack_type=\"({alert_type}[^\"]+)""""
  """virus_name=\"(N\/A|({malware_file_name}[^\"]+))""""
  """Host:\s*({domain}[^\"]+?)((\\r\\n|\s+)[\w\-]+:|\")"""
  """User-Agent:\s*({user_agent}[^"]+?)\s*(\\r\\n[\w\-]+:|")"""
  """geo_location="(N\/A|({country}[^"]+))""""
  """ip_address_intelligence=\"(N\/A|({ip_reputation}[^\"]+))""""
]
ParserVersion = "v1.0.0"


}
```