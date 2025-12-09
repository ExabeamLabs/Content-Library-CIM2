#### Parser Content
```Java
{
Name = "unix-unix-str-endpoint-notification-success-snoopy"
Vendor = Unix
Product = Unix
TimeFormat = ["yyyy-MM-dd'T'HH:mm:ssZ", "yyyy-MM-dd'T'HH:mm:ss.SSSSSS"]
Conditions = ["""snoopy[""", """uid:""", """sid:""", """tty:""", """cwd:""" ]
Fields = [
"""({time}\d{4}-\d{2}-\d{2}T\d{2}:\d{2}:\d{2}.\d+)\S+\s+({host}[\w\-\.]+)\s({process_name}snoopy)\[({process_id}\d+)\]:\s\[login:({user}[\w\.\-]{1,40}\$?)\s+\S+\s+sid:({session_id}\d+)\s+tty:\S+\s\S+\suid:({user_id}\S+)\s+cwd:({folder_name}[^\]]+)\]:\s+({command}[^\]]+)""",
"""({time}\d{4}-\d{2}-\d{2}T\d{2}:\d{2}:\d{2}.\d+)\S+\s+({host}[\w\-\.]+)\s({process_name}snoopy)\[({process_id}\d+)\]:\s\[uid:({user_id}\S+)\s+sid:({session_id}\d+)\s+tty:\S+\scwd:({folder_name}[^\s]+)\sfilename:({file_path}[^\]]+)\]:\s({command}[^\]]+)"""
]
ParserVersion = "v1.0.0"


}
```