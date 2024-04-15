#### Parser Content
```Java
{
Name = "forcepoint-casb-cef-app-activity-skyfence"
Vendor = "Forcepoint"
Product = "Forcepoint CASB"
TimeFormat = "epoch"
Conditions = [
"""CEF"""
"""Skyfence"""
"""|Activity|"""
]
Fields = [
"""\sdvc="+({host}[^"]+)"""
"""\sdvchost="+({host}[^"]+)"""
"""\srt="+({time}\d{13})"""
"""\sduser="+({user}[^"]+)"""
"""\sduser="+[^@]+@({domain}[^".]+)"""
"""\sreason="+({operation}[^"]+)"""
"""\sdestinationServiceName ="({app}[^"]+)""""
"""\sapp="({app}[^"]+)""""
"""\srequestClientApplication=({user_agent}.+?)\s\w+="""
"""\sdst="+({dest_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?"""
"""\ssrc="+({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
"""\sdpriv="+({privileges}[^"]+)"""
"""\sdeviceProcessName ="({object}[^"]+)"+\s\w+="""
"""\smsg="+({additional_info}[^"]+)"""
]
ParserVersion = "v1.0.0"


}
```