#### Parser Content
```Java
{
Name = "liquidfiles-l-json-app-logout-success-logout"
  ParserVersion = v1.0.0
  Conditions = [ """liquidfiles[""", """"message":"Logout User"""  ]

Liquid-json-template = {
    Vendor = "LiquidFiles"
    Product = "LiquidFiles"
    TimeFormat = "MMM dd HH:mm:ss"
    Fields = [
      """({time}\w\w\w \d\d \d\d:\d\d:\d\d)"""
      """({app}liquidfiles)""",
      """"ip":"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""",
      """"message":"({event_name}[^:"]+)""",
      """"username":"(({email_address}[^@"]+@[^\.]+\.[^"]+)|({user}[\w\.\-\!\#\^\~]{1,40}\$?))"""",
      """"hostname":"({host}[^"]+)"""
      """"access_method":({method}[^"]+)""""
      """"user_email":"({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))"""
      """"log_level":"({run_level}[^"]+?)\s*""""
      """"error":"({failure_reason}[^"]+)""""
      """"filename":"({file_name}[^"]+)""""
      ]
    }
  }

  CheckmarxParserTemplates = {
    checkmarx-json-template = {
      Vendor = "Checkmarx"
      Product = "Checkmarx"
      ExtractionType = json
      TimeFormat = "yyyy-MM-dd HH:mm:ss.SSSSSS"
      Fields = [
        """exa_json_path=$.Timestamp,exa_field_name=time""",
        """exa_regex="Timestamp":\s*"({time}[^"]+?)"""",
        """exa_json_path=$.Hostname,exa_field_name=host""",
        """exa_json_path=$.UserName,exa_regex=^(({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))|({user}[\w\.\-]{1,40}\$?))$""",
        """exa_json_path=$.Details,exa_regex=\\?"Username\\?":\s*\\?"(({dest_email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({dest_email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))|({dest_user}[\w\.\-]{1,40}\$?))\\?"""",
        """exa_json_path=$.Details,exa_regex=\\?"UserId\\?":\s*({dest_user_id}\d+)""",
        """exa_json_path=$.OriginIpAddress,exa_regex=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
        """exa_json_path=$.Type,exa_field_name=event_name""",
        """exa_json_path=$.UserId,exa_field_name=user_id""",
        """exa_json_path=$.Details,exa_regex=\\?"TeamName\\?":\s*\\?"({group_name}[^\\"]+)\\?"""",
        """exa_json_path=$.Details,exa_regex=\\?"TeamId\\?":\s*({group_id}\d+)""",
        """exa_json_path=$.Origin,exa_field_name=origin_name"""
      ]
    }
  }

IronscalesParserTemplates = {
    ironscales-cef-template = {
      Vendor = "Ironscales"
      Product = "Ironscales"
      TimeFormat = "MMM dd HH:mm:ss"
      Fields = [
        """({time}\w{3}\s\d\d\s\d\d:\d\d:\d\d)\s+\S+\s+CEF:""",
        """suser=({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))""",
        """duser=({dest_email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({dest_email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))""",
        """cs5=({result}[^=]+?)\s+cs5Label=Report State"""
        """reason=({additional_info}[^=]+?)\s+\w+="""
        """request=({malware_url}[^\s]+)"""
        """cs4=({email_subject}[^=]+?)\s+cs4Label=(?i)(Email Subject)"""
        """CEF:([^\|]+\|){5}(\d+|({event_name}[^\|]+))\|"""
        """cs6=({result}\S+)\s+cs6Label=(?i)Outcome"""
        """cs2=({full_name}[^=]+)\s+cs2Label=Employee Name"""
      ]
    
}
```