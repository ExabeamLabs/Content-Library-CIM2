#### Parser Content
```Java
{
Name = pingidentity-pi-cef-app-authentication-success-authnsessioncreated
  Conditions = [  """CEF:""", """|EAMAuth|""" ,"""|AUTHN_SESSION_CREATED|""" ]
  ParserVersion = "v1.0.0"

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
}

#============================================== Start of PingParsersAA section ==================================================================
PingParsersAA = [
    ${PingParsersTemplates.ping-events}{
Name = "pingidentity-pi-str-endpoint-login-fail-inprogress"
ParserVersion = "v1.0.0"
Conditions = [
"""| AUTHN_ATTEMPT|"""
"""inprogress|"""

}
```