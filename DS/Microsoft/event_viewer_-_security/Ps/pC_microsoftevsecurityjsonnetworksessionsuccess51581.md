#### Parser Content
```Java
{
Name = "microsoft-evsecurity-json-network-session-success-5158-1"
  ParserVersion = "v1.0.0"
  Vendor = "Microsoft"
  Product = "Event Viewer - Security"
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
  Conditions = [
""""event_id":5158"""
"""The Windows Filtering Platform has permitted a bind to a local port"""
  ]
  Fields = [
"""({event_code}5158)"""
"""({event_name}The Windows Filtering Platform has permitted a bind to a local port)"""
""""created"+:\s*"+({time}[^",]+)""""
""""hostname"+:\"+({host}[\w\-.]+)""""
""""ProcessId"+:"+({process_id}[^"]+)""""
""""Application"+:"+({process_path}({process_dir}[^,"]*?[\\\/]+)?({process_name}[^\\\/\s"]+?))""""
""""SourceAddress\"+:"+({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
""""SourcePort"+:"+({src_port}\d+)"""
""""Protocol"+:"+({ms_protocol_num}[^"]+)""""
""""LayerName":"({layer_name}[^"]+)""""
""""computer_name":"({host}({src_host}[\w\-.]+))"""
  ]


}
```