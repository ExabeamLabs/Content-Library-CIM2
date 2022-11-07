#### Parser Content
```Java
{
Name = chcom-c-json-app-login-success-trueclientip
 Vendor = CHCOM
 Product = CHCOM
 ParserVersion = v1.0.0
 TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
 Conditions = ["""chcom_userlogin""", """"secure_log_type":"""", """true_client_ip"""]
 Fields = [
    """"host":\{"name":"({host}[^"]+)""",
    """"@timestamp":"({time}\d{4}-\d{2}-\d{2}T\d{2}:\d{2}:\d{2}\.\d{3}Z)""",
    """"username":"({user}[^"]+)""",
    """"type":"({app}[^"]+)""",
    """"true_client_ip":"({src_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})""",
    """"req_session_id":"({session_id}[^"]+)""",
    """({event_name}login)""",
    """"response_code":"({result}[^"]+)""",
    """"status_code":"({result_code}\d+)""",
    """"log_type":"({service_name}[^"]+)""",
    """"source":"({file_dir}[^"]*[\\\/]+)?({file_name}[^\\\/"]+\.({file_ext}[^\\\/"]+))"""
 ]


}
```