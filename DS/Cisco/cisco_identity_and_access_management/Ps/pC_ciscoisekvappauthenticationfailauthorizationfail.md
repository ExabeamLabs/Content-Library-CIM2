#### Parser Content
```Java
{
Name = "cisco-ise-kv-app-authentication-fail-authorizationfail"
  Vendor = "Cisco"
  Product = "Cisco Identity and Access Management"
  TimeFormat = "MMM dd yyyy HH:mm:ss.SSS"
  Conditions = [
    """Authorization Failed"""
	  """CISE_Alarm"""
    """Failure Reason="""
   ]
  Fields = [
    """CISE_Alarm ({event_category}[^:]+):\s*({event_name}.+?)\s*:"""
    """Failure Reason=({failure_reason}.+?)\s$"""
    """Server=({src_host}[\w\-\.]+)(?:;|$)"""
    """({result}Failed)"""
	"""device IP=({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?"""
	"""Device Name =({dest_host}[\w\-\.]+)"""
  ]
  ParserVersion = "v1.0.0"


}
```