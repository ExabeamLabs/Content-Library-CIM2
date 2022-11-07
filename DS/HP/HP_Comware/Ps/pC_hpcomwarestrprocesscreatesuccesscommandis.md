#### Parser Content
```Java
{
Name = hp-comware-str-process-create-success-commandis
    Vendor = HP
	Product = HP Comware
    TimeFormat = "MMM dd HH:mm:ss yyyy"
    Conditions = [ """-User=""", """-Task=""", """Source: /""", """TAG:""", """Command is""", """-IPAddr=""" ]
    Fields = [
      """({time}\w{3}\s+\d+\s+\d{2}:\d{2}:\d{2}\s+\d{4})\s+({host}[^\s]+)\s+%%""",
      """-User=({user}[^;]+);""",
      """-IPAddr=({src_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})""",
      """-DevIP=({dest_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})""",
      """Command\s*is\s*({process_path}(?:({process_dir}.+?)[\\\/]+)?({process_name}[^\s\\\/]+))\s*Source:""",
      """Command\s*is\s*({process_command_line}.+?)\s*Source:"""
    ]
    DupFields = [ "host->dest_host" ]
	ParserVersion = "v1.0.0"
  

}
```