#### Parser Content
```Java
{
Name = "microsoft-evsecurity-kv-user-privilege-assign-success-4673-1"
ParserVersion = "v1.0.0"
Conditions = [ 
	"""EventCode=4673"""
	"""Microsoft Windows security auditing"""
  """Message=Se llamó a un servicio con privilegios"""
	]
  DupFields = [ "host->dest_host" ]
ParserVersion = "v1.0.0"


}
```