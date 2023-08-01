#### Parser Content
```Java
{
Name = kasada-k-json-http-session-nonstatic
  Vendor = Kasada
  Product = Kasada
  ParserVersion = "v1.0.0"
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
  Conditions = [ """"logType":"HTTP-Transaction"""",""""clientResCode"""",""""access-control-expose-headers"""",""""resourceType":"NON_STATIC_RESOURCE"""" ]
  Fields = [
	""""logType":"({event_category}[^"]+)""""
	""""timestamp":"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d+Z)"""
	""""reason":"({proxy_action}[^"]+)"""
	""""clientResCode":({http_response_code}\d+)"""
	""""clientTokenID":"({client_token}[^"]+?)""""
	""""action":"({action}[^"]+)""""
	""""method":\s*"({method}[^"]+)"""
	""""level":({alert_severity}\d+)"""
	""""ip":"(?:|({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?)""""
	""""url":\s*"({url}[^\"]+)"""
	""""host":"({host}[^"]+)""""
	""""content-type":"({mime}[^"]+)""""
	"""session-id":"({session_id}[^"]+)""""
	""""user-agent":"({user_agent}[^"]+)"""
	""""domain":"({domain}[^"]+)""""
	""""server":"({server}[^"]+)"""
	""""resourceType":\s*"({resource_type}[^"]+)""""
	]


}
```