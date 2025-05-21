#### Parser Content
```Java
{
Name = fortinet-fortiweb-kv-alert-trigger-success-attack
Vendor = Fortinet
Product = Fortiweb Web Application Firewall
TimeFormat = "epoch_sec"
ParserVersion = "v1.0.0"
Conditions = [ """type="attack"""", """sub_type=""", """severity_level=""", """action="Alert""" ]
Fields = [
  """timestamp=({time}\d{10})"""
  """\Wdevname="*({host}[^\s"]+)"*(\s|")"""
  """\Wsrc=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
  """\Wdst=({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?"""
  """src_port=({src_port}\d+)"""
  """dst_port=({dest_port}\d+)"""
  """\Wmain_type="*({alert_name}.+?)["\s]*(\w+=|$)"""
  """\Wsub_type="*({alert_type}.+?)["\s]*(\w+=|$)"""
  """severity_level="({alert_severity}[^"]+)""""
  """user_name="(Unknown|({email_address}[^@"]+@[^\."]+\.[^"]+)|(({domain}[^\\"]+)\\)?({user}[\w\.\-\!\#\^\~]{1,40}\$?))""""
  """proto="*({protocol}[^\s"]+)"""
  """http_agent="(none|({user_agent}[^"]+))"\s\w+="""
  """http_method=({method}[^=]+?)\s\w+="""
  """http_refer="({referrer}[^"]+)"""
  """\Waction="({action}[^"]+)""""
  """msg="({additional_info}[^"=]+)"\s\w+="""
  """http_url="({uri_path}\/[^?\s"]+)?(\?({uri_query}[^"]+))?""""
  """http_host="(none|({web_domain}[^\s]+))""""
  """signature_subclass="({alert_reason}[^"]+)""""
  """\spolicy="({policy_name}[^"]+)""""
  ]


}
```