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
    """"username":"({user}[\w\.\-]{1,40}\$?)""",
    """"type":"({app}[^"]+)""",
    """"true_client_ip":"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
    """"req_session_id":"({session_id}[^"]+)""",
    """({event_name}login)""",
    """"response_code":"({result}[^"]+)""",
    """"status_code":"({result_code}\d+)""",
    """"log_type":"({service_name}[^"]+)""",
    """"source":"({file_dir}[^"]*[\\\/]+)?({file_name}[^\\\/"]+\.({file_ext}[^\\\/"]+))"""
 ]


}
```