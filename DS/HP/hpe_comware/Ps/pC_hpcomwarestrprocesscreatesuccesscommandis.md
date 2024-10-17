#### Parser Content
```Java
{
Name = hp-comware-str-process-create-success-commandis
    Vendor = HP
	Product = HPE Comware
    TimeFormat = "MMM dd HH:mm:ss yyyy"
    Conditions = [ """-User=""", """-Task=""", """Source: /""", """TAG:""", """Command is""", """-IPAddr=""" ]
    Fields = [
      """({time}\w{3}\s+\d+\s+\d{2}:\d{2}:\d{2}\s+\d{4})\s+({host}[^\s]+)\s+%%""",
      """-User=({user}[\w\.\-\!\#\^\~]{1,40}\$?);""",
      """-IPAddr=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
      """-DevIP=({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?""",
      """Command\s*is\s*({process_path}(?:({process_dir}.+?)[\\\/]+)?({process_name}[^\s\\\/]+))\s*Source:""",
      """Command\s*is\s*({process_command_line}.+?)\s*Source:"""
    ]
    DupFields = [ "host->dest_host" ]
	ParserVersion = "v1.0.0"


}
```