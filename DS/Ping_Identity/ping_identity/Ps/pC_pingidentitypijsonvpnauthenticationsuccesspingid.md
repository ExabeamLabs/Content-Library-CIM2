#### Parser Content
```Java
{
Name = "pingidentity-pi-json-vpn-authentication-success-pingid"
Conditions = [
""""source":"PINGID""""
""""type":"user""""
""""status":"POLICY""""
""""message":"""
""""resources":"""
""""result":{"""
]
ParserVersion = "v1.0.0"

cef-ping-events-skyformation = {
  Vendor = Ping Identity
  Product = Ping Identity
  TimeFormat = "epoch"
  Fields = [
    """end=({time}\d{13})""", 
    """cat=(N\/A|({category}[^\s]+))""",
    """destinationServiceName =({app}[^\s]+)""",
    """suser=(anonymous|(({email_address}([A-Za-z0-9]+[!#$%&'+-\/=?^_`~])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)|({user}[\w\.\-\!\#\^\~]{1,40}\$?)))""",
    """"ipAddress":"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""",
    """"source":"({alert_name}[^"]+)"""",
    """"action"*:\{"*type"*:"*({event_name}[^"}]+)"""",
    """"result"*:\{"*status"*:"*({result}[^",]+)""",
    """"message"*:"*({event_name}[^"]+)"""",
    """"idpEntityId"*:"*({file_url}[^"]+)"""",
    """"client"*:\{"*id"*:"*({user_agent}[^"]+)"""",
    """msg=({additional_info}.+?)\soldFile=""",
  cef-ping-events-skyformation = {
  Vendor = Ping Identity
  Product = Ping Identity
  TimeFormat = "epoch"
  Fields = [
    """end=({time}\d{13})""", 
    """cat=(N\/A|({category}[^\s]+))""",
    """destinationServiceName=({app}[^\s]+)""",
    """suser=(anonymous|(({email_address}([A-Za-z0-9]+[!#$%&'+-\/=?^_`~])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)|({user}[\w\.\-\!\#\^\~]{1,40}\$?)))""",
    """"ipAddress":"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""",
    """"source":"({alert_name}[^"]+)"""",
    """"action"*:\{"*type"*:"*({event_name}[^"}]+)"""",
    """"result"*:\{"*status"*:"*({result}[^",]+)""",
    """"message"*:"*({event_name}[^"]+)"""",
    """"idpEntityId"*:"*({file_url}[^"]+)"""",
    """"client"*:\{"*id"*:"*({user_agent}[^"]+)"""",
    """msg=({additional_info}.+?)\soldFile=""",
  ]
}

s-ping-events = {
  Vendor = Ping Identity
  Product = Ping Identity
  ExtractionType = json
  TimeFormat = "MMM dd yyyy HH:mm:ss.SSS"
  Fields = [
    """exa_json_path=$.Time,exa_field_name=time"""
    """exa_json_path=$.duid,exa_regex=(({domain}[^"@\\\/]+)[\\\/]+)?({user}[\w\.\-\!\#\^\~]{1,40}\$?)"""
    """exa_json_path=$.duid,exa_regex=({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.-])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)"""
    """exa_json_path=$.SRCIP,exa_regex=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
    """exa_json_path=$..remoteAddr,exa_regex=({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?"""
    """exa_json_path=$.Status,exa_field_name=result"""
    """exa_json_path=$.Protocol,exa_field_name=protocol"""
    """exa_json_path=$.PingHost,exa_field_name=host"""
    """exa_json_path=$.EventType,exa_field_name=operation"""
    """exa_json_path=$.DescriptionFail,exa_field_name=failure_reason"""
  ]
}

ping-events-3 = {
  Vendor = Ping Identity
  Product = Ping Identity
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Fields = [
    """({time}\d\d\d\d-\d\d-\d\d \d\d:\d\d:\d\d),""",
    """event=({event_name}[^=]+?)\s+(\w+=|$)""",
    """ip=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
    """connectionid=(|({connection_id}[^=]+?))\s+(\w+=|$)""",
    """protocol=(|({protocol}[^=]+?))\s+(\w+=|$)""",
    """pfhost=(|({host}[\w.-]+?))\s+(\w+=|$)""",
    """\sbrowser=\\"({user_agent}[^"]+?)\\?"""",
    """useragent="({user_agent}[^"]+)"""",
    """description="({additional_info}[^"]]+)""""
    """\ssubject="?(||(({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({email_domain}[^\]\-\s"\\,;\|]+\.[^\]\s"\\,;\|\-]+))|(?:[^"]+?:)?({user}[\w\.\-\!\#\^\~]{1,40}\$?)))(\-[^"]+)?"?(,|\s\w+=)"""  ]
}

json-ping-events = {
  Vendor = Ping Identity
  Product = Ping Identity
  ExtractionType = json
  ParserVersion = "v1.0.0"
  TimeFormat = "yyyy-dd-MM'T'HH:mm:ss.SSSZ"
  Fields = [
    """exa_json_path=$.recorded,exa_field_name=time"""
    """exa_json_path=$.client.id,exa_field_name=user_agent"""
    """exa_json_path=$.resources[2].name,exa_field_name=app"""
    """exa_json_path=$.result.status,exa_field_name=result"""
    """exa_json_path=$.result.message,exa_field_name=result_reason"""
    """exa_json_path=$.source,exa_field_name=alert_source"""
    """exa_json_path=$.action.type,exa_field_name=event_name"""
    """exa_json_path=$.resources.subject,exa_field_name=operation"""	
    """exa_regex="ipAddress":\s*"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""",
    """exa_regex="actors":[^}]+?"name":"(({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.-])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)|({user}[\w\.\-\!\#\^\~]{1,40}\$?))"[^}]+?"type":"user"""",
    """exa_regex="actors":[^}
}
```