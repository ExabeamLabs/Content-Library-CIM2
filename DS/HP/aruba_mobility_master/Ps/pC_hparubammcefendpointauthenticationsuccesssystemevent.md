#### Parser Content
```Java
{
Name = hp-arubamm-cef-endpoint-authentication-success-systemevent
  Vendor = HP
  Product = Aruba Mobility Master
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Conditions = [ """CEF:""", """|Aruba|""", """|SystemEvent|""", """'authenticated'""" ]
  Fields = [
    """dvchost=({host}[^\s]+)""",
    """\sIP=\?*\s*({event_name}[^"]+)""",
	  """deviceProcessName =({process_name}.+?)\s+(\w+=|$)""",
	  """\Wmsg=(|({additional_info}.+?))("|$)""",
	  """MAC\\*=({src_mac}([a-fA-F\d]{2}[-:]){5}[a-fA-F\d]{2})""",
	  """from\s+(({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))|({src_host}[^\s:]+))"""
  ]
	ParserVersion = v1.0.0


}
```