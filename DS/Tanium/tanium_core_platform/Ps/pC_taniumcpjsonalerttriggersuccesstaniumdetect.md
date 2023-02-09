#### Parser Content
```Java
{
Name = tanium-cp-json-alert-trigger-success-taniumdetect
    ParserVersion = v1.0.0
    Vendor = Tanium
    Product = Tanium Core Platform
    TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
    Conditions = [ """TaniumDetect""", """Timestamp""", """Computer Name""", """Computer IP""" ]
    Fields = [
      """"Timestamp":"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d.\d\d\dZ)"""",
      """"User Name":"({user}[^",]+?)"""",
      """"User Id":"({user}[^",]+?)"""",
      """"User Domain":"({domain}[^",]+?)"""",
      """"user\\*":\\*"((NT-AUTORITÄT|NT AUTHORITY|({domain}[^"\\]+))\\+)?(Système|SYSTEM|({user}[^"]+?))\\*"""",
      """"Priority":"({alert_severity}[^",]+)"""",
      """"Event Name":"({alert_name}[^",]+)"""",
      """"Event Name":"({alert_type}[^",]+)"""",
      """"type\\*":\\*"({alert_type}[^"]+?)\\*"""",
      """"Event Id":"({alert_id}[^",]+)"""",
      """"Computer Name":"({src_host}[^"]+?)"""",
      """"Computer IP":"({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""",
      """"name\\*":\\*"({file_name}[^"]+?)\\*"""",
      """"source\\*":\\*"({log_source}[^"]+?)\\*"""",
      """"Intel Name"+:"+({alert_name}[^"]+)""",
      """"Intel Type"+:"+({alert_type}[^"]+)""",
      """"Intel Labels":"({additional_info}[^"]+)""",
      """"properties\\?"+:[^\]]+?md5\\?"+:\\?"+({hash_md5}[^"]+?)\\?"""",
      """"properties\\?"+:[^\]]+?args\\?"+:"*\\*"+({process_command_line}[^,\]]+?)\\?\s*","cwd""", 
      """"properties\\?"+:[^\]]+?fullpath\\?"+:\\?"+({process_path}({process_dir}[^"]+)\\+({process_name}[^"]+))\\+""""    
      ]


}
```