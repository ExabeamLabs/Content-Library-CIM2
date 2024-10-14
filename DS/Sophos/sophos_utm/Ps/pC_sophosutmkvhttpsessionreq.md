#### Parser Content
```Java
{
Name = "sophos-utm-kv-http-session-req"
Vendor = "Sophos"
Product = "Sophos UTM"
TimeFormat = "epoch_sec"
Conditions = [
  """req="""
  """meth="""
  """ t="""
]
Fields = [
  """\st=({time}\d{10})"""
  """\d\d:\d\d:\d\d ({host}[\w\-.]+)"""
  """\starget_ip=\"({dest_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})\""""
  """\sh=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
  """\ss=({http_response_code}\d+)"""
  """\su=\"(-|(({domain}[^\\]+)\\+)?({user}[\w\.\-\!\#\^\~]{1,40}\$?))"""
  """\sact=(-|({action}.+?))\s+(\w+=|$)"""
  """\smeth=\"*(-|({method}[^\"\s]+))"""
  """\sout=(-|({bytes_out}\d+))"""
  """\sin=(-|({bytes_in}\d+))"""
  """\sreq=\"(-|\w+\s+({url}\S+))"""
  """\sreq=\"(-|(\w+\s+({protocol}[^:]+)))"""
  """\sdom=\"(-|({web_domain}[^\"]+))"""
  """\sreq=\"(-|(\w+\s\w+:\/+[^\/]+\/({uri_path}[^?\s\"]+)))"""
  """\sreq=\"(-|(\w+\s\w+:\/+[^?]+({uri_query}\?[^\s\"]+)))"""
  """\stype=\"(-|({mime}[^\"]+))"""
  """\sua=\"(-|({user_agent}[^\"]+))"""
  """\scat=\"(-|0x2({risk_level}\d)({event_category}[^\"]+))"""
]
ParserVersion = "v1.0.0"


}
```