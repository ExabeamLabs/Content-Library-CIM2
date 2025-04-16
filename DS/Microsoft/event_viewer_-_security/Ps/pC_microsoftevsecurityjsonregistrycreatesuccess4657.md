#### Parser Content
```Java
{
Name = "microsoft-evsecurity-json-registry-create-success-4657"
  Vendor = "Microsoft"
  Product = "Event Viewer - Security"
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
  Conditions = [ """"event_id":4657""", """A registry value was modified""", """"ObjectName":""" ]
  Fields = [
	"""({event_name}A registry value was modified)"""
    """({event_code}4657)"""
	""""hostname":"({host}[^"]+)""""
	"""@timestamp"+:"+({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d\d\dZ)""""
	"""SubjectLogonId"+:"+({login_id}[^"]+)""""
	"""SubjectUserName"+:"+({user}[\w\.\-\!\#\^\~]{1,40}\$?)""""
	"""SubjectDomainName"+:"+({domain}[^"]+)""""
	""""ProcessId":"({process_id}[^"]+)""""
	""""ObjectName":"({registry_key}[^"]+)""""
	""""ObjectValueName":"({registry_value}[^"]+)""""
	""""HandleId":"({object_id}[^"]+)""""
	""""NewValueType":"({registry_details_type}[^"]+)""""
	""""NewValue":"({registry_details}[^"]+)""""
	""""OldValueType":"({old_registry_details_type}[^"]+)""""
	""""OldValue":"({old_registry_details}[^"]+)""""
	""""ProcessName":"({process_path}({process_dir}[^"]+[\\\\]+)({process_name}[^"]+))""""
	""""OperationType":"({operation}[^"]+)""""
  ]
  ParserVersion = "v1.0.0"
  DupFields = [ "host->src_host", "user->src_user", "domain->src_domain" ]


}
```