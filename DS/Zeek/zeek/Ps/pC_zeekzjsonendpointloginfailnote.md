#### Parser Content
```Java
{
Name = "zeek-z-json-endpoint-login-fail-note"
Product = "Zeek"
Conditions = [
  """note":"SSL::Invalid_Server_Cert""""
  """"id.orig_h":"""
  """"id.resp_h":"""
]
ExtractionType = json
ParserVersion = "v1.0.0"

auth0-authentication-template.Fields}[
    """exa_regex=({operation_type}fcp)""",
    """user_id"+:"+((({auth_type}[^|"]+)\|({domain}[^|"]+)\|(({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.-])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)|({dest_user}[\w\.\-]{1,40}\$?)))|(({=auth_type}[^|"]+)\|[^\|"@]+))"""",
    """user_name"+:"+(({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+))|({dest_user}[\w\.\-]{1,40}\$?))"""",
    """exa_regex="user_name":"(({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+))|({dest_user}[\w\.\-]{1,40}\$?))"""
    """exa_regex="user_id":"((({auth_type}[^|"]+)\|({domain}[^|"]+)\|(({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.-])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)|({dest_user}[\w\.\-]{1,40}\$?)))|(({=auth_type}[^|"]+)\|[^\|"@]+))"""",
    """exa_json_path=$..user_name,exa_regex=(({dest_user}[\w\.\-\!\#\^\~]{1,40}\$?)(@({domain}[^"]+))?|)"""
    """exa_json_path=$..user_name,exa_regex=(({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+))|({dest_user}[\w\.\-]{1,40}\$?))"""
  ]
  ParserVersion = "v1.0.0"
},

{
Vendor = Auth0
Product = Auth0
TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
Fields = [
      """exa_json_path=$..date,exa_field_name=time"""
      """exa_json_path=$..hostname,exa_field_name=host"""
      """exa_json_path=$.message.description,exa_field_name=additional_info"""
      """exa_json_path=$..ip,exa_regex=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
      """exa_json_path=$..user_name,exa_regex=(({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+))|({user}[\w\.\-]{1,40}\$?))"""
      """exa_json_path=$..user_id,exa_field_name=user_id"""
      """exa_json_path=$..user_id,exa_regex=((({auth_type}[^|"]+)\|({domain}[^|"]+)\|[^\|]*?)|(({=auth_type}[^|"]+)\|))"""
      """exa_json_path=$..client_name,exa_field_name=app"""
      """exa_json_path=$..user_agent,exa_field_name=user_agent"""
      """exa_json_path=$..severity,exa_field_name=alert_severity"""
      """exa_json_path=$.message.type,exa_regex=({operation_type}[^",]+)"""
      """exa_regex=({operation_type}f)"""
      """exa_json_path=$.message.details.error.message,exa_field_name=failure_reason"""
]
ExtractionType = json
Name = auth0-a-json-endpoint-login-fail-invalidrequest
Conditions = [
  """type":"f""""
  """connection_id"""
  """client_id"""
]
ParserVersion = "v1.0.0"
},

{
Vendor = Auth0
Product = Auth0
TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
Fields = [
  """exa_json_path=$..date,exa_field_name=time"""
      """exa_json_path=$..hostname,exa_field_name=host"""
      """exa_json_path=$.message.description,exa_field_name=additional_info"""
      """exa_json_path=$..ip,exa_regex=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
      """exa_json_path=$..user_name,exa_regex=(({user}[\w\.\-\!\#\^\~]{1,40}\$?)(@({domain}[^,]+))?)"""
      """exa_json_path=$..user_id,exa_regex=((({auth_type}[^|"]+)\|({domain}[^|"]+)\|({user}[\w\.\-\!\#\^\~]{1,40}\$?))|(({=auth_type}[^|"]+)\|))"""
      """exa_json_path=$..client_name,exa_field_name=app"""
      """exa_json_path=$..user_agent,exa_field_name=user_agent"""
      """exa_json_path=$..severity,exa_field_name=alert_severity"""
      """exa_json_path=$.message.type,exa_regex=({operation_type}[^",]+)"""
      """exa_regex=({operation_type}f)"""
      """exa_json_path=$.message.details.error.message,exa_field_name=failure_reason"""
]
ExtractionType = json
Name = auth0-a-json-endpoint-login-fail-invalidrequest-1
Conditions = [
  """type":"f""""
  """user_id"""
  """"hostname":""""
]
ParserVersion = "v1.0.0"
},

{
  Name = avaya-ers-str-endpoint-login-fail-intruderip
  Vendor = Avaya
  Product = Avaya Ethernet Routing Switch
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Conditions = [ """:Authentication Failure""", """Server IP""", """Intruder IP""" ]
  Fields = [
    """({event_name}Authentication Failure)""",
    """Server IP\s+({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?""",
    """Intruder IP\s+({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
  ]
  ParserVersion = "v1.0.0"
},

{
  Name = axway-gateway-str-endpoint-login-success-edge
  Vendor = Axway
  Product = Axway Gateway
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Conditions = [ """edge_source=""", """edge_host=""", """edge_fleet=""", """Axway""" ]
  Fields = [
    """edge_source="({additional_info}[^=]+?)"\s+\w+"""
    """edge_host="({edge_host}[^=]+?)"\s+\w+"""
    """edge_fleet="({edge_fleet}[^"]+)"""
    """({time}\d+-\d+-\d+\s\d+:\d+:\d+)"""
    """\s(({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))|({dest_host}[\w\-\.]+))\s({bytes}\d+)\s+({file_path}(({file_dir}[^=]+?)[\\\/]+)?({file_name}[^\\\/]*?(\.({file_ext}\w+))?))\s+({category}[a-z])\s+({secured}[a-z])\s+({edge_response_status}[a-z])\s+({access_type}[a-z])\s+(({email_address}([A-Za-z0-9]+[!#$%&'+-\/=?^_`~])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,\|]+\.[^\]\s"\\,\|'\\_]+))|({user}[\w\.\-\!\#\^\~]{1,40}\$?))\s+({server_name}[^\s]+)\s"""
  ]
  ParserVersion = "v1.0.0"  
},

{
  Name = barracuda-firewall-str-endpoint-login-fail-denied
  Vendor = Barracuda
  Product = Barracuda Cloudgen Firewall
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Conditions = [ """ LOGIN ATTEMPT: """, """ Security """, """: Denied: """, """: Login """, """box_Auth_access:""" ]
  Fields = [
    """\d\d:\d\d:\d\d\s({host}\S+)""",
    """Login (|({user}[\w\.\-\!\#\^\~]{1,40}\$?)\s)from ({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?\s*:\s*({action}[^:.]+)(:|\.)""",
    """({event_name}LOGIN ATTEMPT)""",
    """Denied:\s({failure_reason}[^$]+?)\s*$"""
  ]
  ParserVersion = "v1.0.0"
},

{
  Name = barracuda-firewall-str-endpoint-login-allowed
  Vendor = Barracuda
  Product = Barracuda Cloudgen Firewall
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Conditions = [ """ LOGIN ATTEMPT: """, """ Info """, """ : Allowed""", """box_Auth_access:""", """: Login """ ]
  Fields = [
    """\d\d:\d\d:\d\d\s({host}\S+)""",
    """Login (|({user}[\w\.\-\!\#\^\~]{1,40}\$?)\s)from ({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?\s*:\s*({action}[^:.]+)(:|\.)""",
    """({event_name}LOGIN ATTEMPT)"""
  ]
  ParserVersion = "v1.0.0"
},




{
Vendor = "Dell"
Product = "EMC Isilon"
TimeFormat = "yyyy-MM-dd'T'HH:mm:ssZ"
Fields = [
"""({time}\d+-\d+-\d+T\d+:\d+:\d+[\+\-]+\d+:\d+)"""
"""({time}\d+-\d+-\d+T\d+:\d+:\d+(([\+\-]\d+:\d+)|Z))\s+({host}[\w\-.]+)\s+([^\[\s]*)?\[[^\]]*\]:?\s+({user_sid}[^\s\|]+)\|({user_uid}[^\|]*)\|({src_zone}[^\|]+)\|({zone_id}[^\|]*)\|({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?\|({protocol}[^\|]*)\|({access}OPEN)\|({result}[^\|\s]*)\|({desire_access}[^\|]*)\|({file_type}[^\|]*)\|({create_result}[^\|]*)\|(|({inode}[^\|]*))\|({file_path}({file_dir}[^"]+[\\\/])?({file_name}[^"]+(\.({file_ext}[^"]+)?)\s+)?)""",
"""\d+-\d+-\d+T\d+:\d+:\d+[\+\-]+\d+:\d+\s+({host}[\w\-.]+)\s"""
"""({user_sid}[^\s\|:\]]+)\|([^\|]*\|){3}({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?\|({protocol}[^\|]+)\|({access}[^\|]+)\|({action}SUCCESS|FAILED)(:({failure_code}[^\|]*))?\|([^\|]*\|)?({file_type}FILE|DIR)\|"""
"""\|({file_path}({src_file_path}({file_dir}[^"\|][^\|,]*?[\\\/]+)?(|({file_name}[^\\\/\|]*?(\.({file_ext}({src_file_ext}[^\s"\.]+)))?))))\s*$"""
"""\|FAILED:.*?\|(FILE|DIR)\|({failure_reason}[^\|]+)"""
]
Name = "dell-emcisilon-str-file-read-success-open-1"
Conditions = [
""" Isilon"""
"""|OPEN|SUCCESS|"""
]
ParserVersion = "v1.0.0"
},

{
  Name = dell-emcisilon-str-file-read-success-open
  ParserVersion = v1.0.0
  Vendor = Dell
  Product = EMC Isilon
  TimeFormat = ["yyyy-MM-dd'T'HH:mm:ssZ","yyyy-MM-dd'T'HH:mm:ss.SSSSSSZ"]
  Conditions = [ """|SMB|""","""|OPEN|""" ]
  Fields = [
    """({time}\d+-\d+-\d+T\d+:\d+:\d+(([\+\-]\d+:\d+)|Z))\s+({host}[\w\-.]+)\s+([^\[\s]*)?\[[^\]]*\]:?\s+({user_sid}[^\s\|]+)\|({user_uid}[^\|]*)\|({src_zone}[^\|]+)\|({zone_id}[^\|]*)\|({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?\|({protocol}[^\|]*)\|({access}OPEN)\|({result}[^\|\s]*)\|({desire_access}[^\|]*)\|({file_type}[^\|]*)\|({create_result}[^\|]*)\|(|({inode}[^\|]*))\|({file_path}({file_dir}[^"]+[\\\/])?({file_name}[^"]+(\.({file_ext}[^"]+)?)\s+)?)""",
    """({time}\d+-\d+-\d+T\d+:\d+:\d+\.\d+(([\+\-]\d+:\d+)|Z))\s+({host}[\w\-.]+)\s+.+?\s+({user_sid}[^\s\|]+)\|({user_uid}[^\|]*)\|({src_zone}[^\|]+)\|({zone_id}[^\|]*)\|({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?\|({protocol}[^\|]*)\|({access}OPEN)\|({result}[^\|\s]*)\|({desire_access}[^\|]*)\|({file_type}[^\|]*)\|({create_result}[^\|]*)\|(|({inode}[^\|]*))\|({file_path}({file_dir}[^"]+[\/])?({file_name}[^"]+(\.({file_ext}[^\\"]+)?)\s+)?)"""
  
}
```