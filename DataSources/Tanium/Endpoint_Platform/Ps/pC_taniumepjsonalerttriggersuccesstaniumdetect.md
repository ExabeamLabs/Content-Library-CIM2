#### Parser Content
```Java
{
Name = tanium-ep-json-alert-trigger-success-taniumdetect
    ParserVersion = v1.0.0
    Vendor = Tanium
    Product = Endpoint Platform
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
      """"Computer IP":"({src_ip}[a-fA-F\d.:]+)"""",
      """"fullpath\\*":\\*"({malware_url}[^"]+?)\\*"""",
      """"name\\*":\\*"({file_name}[^"]+?)\\*"""",
      """"source\\*":\\*"({log_source}[^"]+?)\\*"""",
      """"Intel Name"+:"+({alert_name}[^"]+)""",
      """"Intel Type"+:"+({alert_type}[^"]+)""",
      """"Intel Labels":"({additional_info}[^"]+)"""
    ]


}
```