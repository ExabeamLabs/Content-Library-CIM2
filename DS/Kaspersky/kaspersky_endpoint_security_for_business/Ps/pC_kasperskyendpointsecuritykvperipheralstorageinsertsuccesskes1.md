#### Parser Content
```Java
{
Name = kaspersky-endpointsecurity-kv-peripheral-storage-insert-success-kes-1
  Vendor = Kaspersky
  Product = Kaspersky Endpoint Security for Business
  TimeFormat =  "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
  Conditions = [ """ KES|""", """ tdn="""", """ hdn="""", """VID y PID de dispositivo:""" ]
  Fields = [
    """({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d\d\dZ) ({host}[\w\-.]+) KES\|""",
    """hip="({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?""",
    """hdn="({dest_host}[^"]+)""",
    """Tipo de dispositivo\/Tipo de bus:\s*({device_class}[^"\\]+)""",
    """Id. de dispositivo:\s*({device_id}.+)&\d+""",
    """Usuario:\s*(({domain}[^"\\]+)\\+)?({user}[\w\.\-\!\#\^\~]{1,40}\$?)""",
    """Resultado\\Decisión:\s*({action}[^"\\]+)""",
    """Operación:\s*({operation}[^\"]+)""",
    """etdn="({operation_details}[^"]+)""",
    """USB\\+VID_({device_vid}[^&]+)&PID_({device_pid}[^\\&]+)"""
  ]
  DupFields = [ "operation_details->alert_name","action->alert_type","operation->result" ]
  ParserVersion = "v1.0.0"


}
```