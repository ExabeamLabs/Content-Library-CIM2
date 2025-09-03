#### Parser Content
```Java
{
Name = "f5-asm-kv-alert-trigger-success-botdefense"
Vendor = "F5"
Product = "F5 Application Security Manager"
TimeFormat = "MMM dd yyyy HH:mm:ss"
Conditions = [ """device_product="Application Security Module"""", """device_vendor="F5"""", """bot_name=""", """bot_signature=""" ]
Fields = [
  """,request_date_time="({time}\w+\s\d+\s\d{4}\s\d+\:\d+\:\d+)""",
  """^hostname="({host}[^"]+)""",
  """bigip_mgmt_ip="({device_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})""",
  """client_ip="({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
  """client_ip_geo_location="({src_country_code}[^"]+)""",
  """client_port="({src_port}\d+)""",
  """client_request_uri="({url}[^"]+)""",
  """dest_ip="({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?""",
  """dest_port="({dest_port}\d+)""",
  """http_method="({method}[^"]+)""",
  """http_protocol_indication="({protocol}[^"]+)""",
  """virtual_server_name="({server_name}[^"]+)""",
  """http_protocol_info="({version}[^"]+)""",
  """host="({web_domain}[^"]+)""",
  """,action="({action}[^"]+)""",
  """,request_status="({state}[^"]+)""",
  """session_id="({session_id}[^"]+)""",
  """http_request="({additional_info}[\S\s]+)"""",
  """User-Agent:\s({user_agent}[^"]+)\\r\\nAccept:""",
  """Cookie:\s({request_cookie}[\S\s]+)\\r\\nReferer:""",
  """Referer:\s({referrer}[^"]+)"""
  ]
ParserVersion = "v1.0.0"


}
```