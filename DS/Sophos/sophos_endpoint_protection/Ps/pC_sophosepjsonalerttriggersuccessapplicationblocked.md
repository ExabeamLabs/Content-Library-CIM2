#### Parser Content
```Java
{
Name = sophos-ep-json-alert-trigger-success-applicationblocked
Vendor = Sophos
Product = Sophos Endpoint Protection
TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
Conditions = [
  """"Event::Endpoint::Application::Blocked""""
  """"Controlled application blocked: """
]
Fields = [
  """"location":"({host}[^"]+)"""
  """"when":"({time}\d\d\d\d\-\d\d\-\d\dT\d\d:\d\d:\d\d\.\d\d\dZ)"""
  """"rt":\s*"({time}\d\d\d\d\-\d\d\-\d\dT\d\d:\d\d:\d\d\.\d\d\dZ)"""
  """"name":\s*"({alert_name}[^:]+):\s({target}[^"]+)"""
  """"name":\s*"({additional_info}[^"]+)"""
  """"type":\s*"({alert_type}[^"]+)"""
  """"dhost":\s*"({src_host}[^"]+)"""
  """"severity":\s*"({alert_severity}[^"]+)"""
  """"suser":\s*"(?:n\/a|({full_name}[^"\\,]+))""""
  """"suser":\s*"({last_name}[^",\s]+),\s*({first_name}[^,"\s]+)""""
  """"suser":\s*"(({domain}[^\\",]+)\\+)?({user}[\w\.\-]{1,40}\$?)""""
  """"source":"({full_name}[^",]+)""""
  """"source":"({last_name}[^",\s]+),\s*({first_name}[^,"\s]+)""""
  """\\"source_info\\"__ip=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
  """"id":\s*"({alert_id}[^"]+)"""
]
DupFields = [
  "host->src_host"
]
ParserVersion = "v1.0.0"


}
```