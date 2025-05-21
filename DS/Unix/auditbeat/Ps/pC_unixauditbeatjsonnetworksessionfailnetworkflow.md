#### Parser Content
```Java
{
Name = unix-auditbeat-json-network-session-fail-networkflow
Vendor = "Unix"
Product = "Auditbeat"
TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
Conditions = [
  """"auditbeat""""
  """"action":"network_flow""""
  """"process":"""
  """"pid":"""
]
Fields = [
  """timestamp":"({time}\d+-\d+-\d+T\d+:\d+:\d+\.\d+Z)""""
  """"host":.+?"name":"({host}[\w\-\.]+)""""
  """"destination":.+?"ip":"({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?""""
  """"source".+?"ip":"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""""
  """"process":.+?"name":"\s*({process_path}({process_dir}([^"]+)?[\\\/])?({process_name}[^\\\/"]+))""""
  """"process".+?"executable":"({process_path}(({process_dir}[^"]*?)\/)?[^"\\\/]*?)""""
  """"source":.+?"port":({src_port}\d+)"""
  """"destination":.+?"port":({dest_port}\d+)"""
  """"network":.+?"direction":"(unknown|({direction}[^"]+))""""
  """"network":.+?"bytes":({bytes}\d+)"""
  """"domain":"({domain}[^"]+)""""
  """"user":\{.+?name":"({user}[\w\.\-\!\#\^\~]{1,40}\$?)""""
  """"process":.+?"pid":({process_id}\d+)"""
  """"complete":({result}[^,}]+)"""
  """"action":"({action}[^"]+)""""
]
DupFields = [
  "action->event_name"
]
ParserVersion = "v1.0.0"


}
```