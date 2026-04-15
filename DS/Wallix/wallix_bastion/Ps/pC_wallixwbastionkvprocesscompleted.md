#### Parser Content
```Java
{
Name = wallix-wbastion-kv-process-completed
  Vendor = Wallix
  Product = Wallix Bastion
  TimeFormat = "MMM dd HH:mm:ss"
  Conditions = [ """rdpproxy[""", """[RDP Session]""", """user=""", """ type=""""]
  Fields = [
     """<\d+>({time}\S+\s\d+\s\d{2}:\d{2}:\d{2})""",
     """({process_name}rdpproxy)\[({process_id}\d+)\]""",
     """session_id="({session_id}[^"]+)"""",
     """client_ip="({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))"""",
     """target_ip="({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))"""",
     """user="({user}[\w\.\-]{1,40}\$?)"""",
     """device="({host}[\w\.\-]+)"""",
     """command_line="({process_command_line}[^\$]+)"""",
     """service="({dest_service_name}[^"]+)""",
     """account="({account_name}[^"]+)""",
     """type="({operation_type}[^"]+)"""
    ]
    ParserVersion = "v1.0.0"


}
```