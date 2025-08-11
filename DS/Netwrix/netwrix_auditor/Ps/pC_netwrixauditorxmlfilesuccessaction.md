#### Parser Content
```Java
{
Name = "netwrix-auditor-xml-file-success-action"
Vendor = "Netwrix"
Product = "Netwrix Auditor"
TimeFormat = "yyyy-MM-dd'T'HH:mm:ssZ"
Conditions =  [ """<EventRecordID>""", """ Action : """, """ ObjectType : """, """ What : """ ]
Fields = [
  """When\s*:\s*({time}\d+-\d+-\d+T\d+:\d+:\d+Z)"""
  """<Computer>({host}[\w\-.]+)"""
  """>({event_code}\d+)<\/EventID>"""
  """<EventRecordID>({event_id}.+?)<\/EventRecordID>"""
  """Action\s*:\s*({access}.+?)\s*Message\s*:"""
  """Where\s*:\s*({dest_host}[\w\-.]+)"""
  """ObjectType\s*:\s*({file_type}.+?)\s*Who\s*:"""
  """Who\s*:\s*(({domain}[^\\\s]+)\\+)?(system|({user}[\w\.\-\!\#\^\~]{1,40}\$?))"""
  """What\s*:\s*(|({file_path}({file_dir}[^\"]*?)[\\\/]*({file_name}[^\\\"]+?(\.({file_ext}[^\\\.\s\"]+))?)))\s*When\s*:"""
  """Workstation\s*:\s*(|({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?)\s*Details\s*:"""
]
ParserVersion = "v1.0.0"


}
```