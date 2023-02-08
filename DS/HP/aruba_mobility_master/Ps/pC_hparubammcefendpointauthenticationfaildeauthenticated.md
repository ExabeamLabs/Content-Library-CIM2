#### Parser Content
```Java
{
Name = hp-arubamm-cef-endpoint-authentication-fail-deauthenticated
  Vendor = HP
  Product = Aruba Mobility Master
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Conditions = [ """CEF:""", """|Aruba|""", """|SystemEvent|""", """deauthenticated:""" ]
  Fields = [
    """dvchost=({host}[^\s]+)""",
	  """deviceProcessName =({process_name}.+?)\s+(\w+=|$)""",
	  """\Wmsg=(|({additional_info}.+?))("|$)""",
	  """MAC\\*=({src_mac}([a-fA-F\d]{2}[-:]){5}[a-fA-F\d]{2})""",
  ]
	ParserVersion = v1.0.0


}
```