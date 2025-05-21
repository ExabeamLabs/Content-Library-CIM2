#### Parser Content
```Java
{
Name = hp-arubamm-cef-user-create-success-useradded
  Vendor = HP
  Product = Aruba Mobility Master
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Conditions = [ """CEF:""", """|Aruba|""", """|SystemEvent|""", """User entry added:""", """deviceProcessName""" ]
  Fields = [
    """dvchost=({host}[^\s]+)""",
    """deviceProcessName =({process_name}.+?)\s+(\w+=|$)""",
    """reason=({additional_info}[^"]+)""",
    """MAC\\*=({src_mac}([a-fA-F\d]{2}[-:]){5}[a-fA-F\d]{2})""",
    """IP=({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?""",
  ]
	ParserVersion = v1.0.0


}
```