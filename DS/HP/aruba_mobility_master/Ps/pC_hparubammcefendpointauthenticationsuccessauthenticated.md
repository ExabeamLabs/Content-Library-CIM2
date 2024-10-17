#### Parser Content
```Java
{
Name = hp-arubamm-cef-endpoint-authentication-success-authenticated
  Vendor = HP
  Product = Aruba Mobility Master
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Conditions = [ """CEF:""", """|Aruba|""", """|SystemEvent|""", """ Authenticated """ ]
  Fields = [
    """dvchost=({host}[^\s]+)""",
    """\sAM:\s*({event_name}[^"]+)""",
    """deviceProcessName =({process_name}.+?)\s+(\w+=|$)""",
    """\Wmsg=(|({additional_info}.+?))("|$)"""
    """AP\s(({full_name}({first_name}[A-Z][a-z]+)\s+({last_name}\w*))|({user}[\w\.\-\!\#\^\~]{1,40}\$?))@({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))"""
  ]
	ParserVersion = v1.0.0


}
```