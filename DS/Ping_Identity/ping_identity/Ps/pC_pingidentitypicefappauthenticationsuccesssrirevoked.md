#### Parser Content
```Java
{
Name = pingidentity-pi-cef-app-authentication-success-srirevoked
  ParserVersion = "v1.0.0"
  Conditions = [  """|EAMAuthSI|""", """|SRI_REVOKED|""", """|signin-si|""" ]

ping-auth-events{
   Vendor = Ping Identity
   Product = Ping Identity
   TimeFormat = "MMM dd yyyy HH:mm:ss.SSS"
   Fields = [
     """dvchost=({host}[^\s]+)""",
     """rt=({time}\w+\s\d\d\s\d\d\d\d\s\d\d:\d\d:\d\d.\d\d\d)""",
     """src=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
     """msg=({result}[^\s]+)""",
     """cs3=\(\w+:({protocol}[^\s]+)\)""", 
     """cs5=({user}[\w\.\-]{1,40}\$?)""",
     """CEF:([^\|]*\|){3}({event_name}[^\|]+)\|""",
     """cs8=({user_agent}[^=]+?)\s+\w+=""",
     """cs7=(|({additional_info}[^\n]+?))\s+cs8Label="""
   ]   
},

pingone-events = {
   Vendor = Ping Identity
   Product = PingOne
   TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
   ExtractionType = json
   Fields = [
      """exa_json_path=$.recordedAt,exa_field_name=time""",
      """exa_json_path=$.action.type,exa_field_name=operation""",
      """exa_json_path=$.action.description,exa_field_name=event_name""",
      """exa_json_path=$.source.userAgent,exa_field_name=user_agent""",
      """exa_json_path=$.actors.client.name,exa_field_name=client_name""",
      """exa_json_path=$.actors.client.id,exa_field_name=client_id""",
      """exa_json_path=$.actors.client.type,exa_field_name=client_type""",
      """exa_json_path=$.result.status,exa_field_name=result""",
      """exa_json_path=$.result.description,exa_field_name=additional_info""",
      """exa_json_path=$.correlationId,exa_field_name=correlation_id""",
      """exa_json_path=$.source.ipAddress,exa_field_name=src_ip""",
      """exa_regex="user":.+?"name":"(({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))|({user}[\w\.\-]{1,40}\$?))"""",
      """exa_regex="resources":.+?"name":"(({dest_email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({dest_email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))|({dest_user}[\w\.\-]{1,40}\$?))""""
   
}
```