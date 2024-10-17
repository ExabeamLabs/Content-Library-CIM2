#### Parser Content
```Java
{
Name = "cisco-iws-cef-http-session-ironportwebsecurityappliance"
Vendor = "Cisco"
Product = "IronPort Web Security"
TimeFormat = "epoch"
Conditions = [
"""|CISCO|IronPort Web Security Appliance|"""
"""categorySignificance="""
]
Fields = [
"""\srt=({time}\d{13})"""
"""\sdvc=({host}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})"""
"""\sdvchost=({host}[^\s]+)"""
"""\sdst=({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?"""
"""\srequest=({dest_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})(:({dest_port}\d+))?"""
"""\ssrc=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
"""\sduser=(({domain}[^\s\\]+)\\+)?({user}[\w\.\-\!\#\^\~]{1,40}\$?)(@({=domain}[^"=\s]+))?\s\w+="""
"""\sact=(?:NONE|({proxy_action}.+?))\s\w+="""
"""\scategoryOutcome=\/({action}.+?)\s\w+="""
"""\srequestMethod=({method}.+?)\s\w+="""
"""\sout=({bytes_out}\d+)\s\w+="""
"""\sin=({bytes_in}\d+)\s\w+="""
"""\|CISCO\|IronPort Web Security Appliance\|[^|]*\|({http_response_code}\d+)\|"""
"""\sdhost=(?:-|({web_domain}.+?))\s\w+="""
"""\smsg=(?:-|(\w+\s+({protocol}[^:]+))):\/\/"""
"""\srequest=(-|({url}\S+))"""
"""\srequest=(?:-|(\w+:\/+[^\/]+\/({uri_path}.+?)))(\?.+?)?\srequestMethod="""
"""\smsg=(?:-|(\w+\s+\w+:\/+[^?]+({uri_query}\?.+?)))\sin="""
"""\scs2=(?:-|({user_agent}.+?))\s\w+="""
"""\scs3=(?:ns|({original_risk_score}\d+))\s\w+="""
"""\scs4=.+?(KHTML,)?([^,]*,){19}(?:(-|nc|Unknown)|({category}[^,]+))"""
"""\scs4=.+?(KHTML,)?([^,]*,){22}\"*(?:(-|Unknown|nc)|({category}[^\",]+))"""
"""\sfileType=(?:-|({mime}.+?))\s\w+="""
]
DupFields = [
"user->orig_user"
]
ParserVersion = "v1.0.0"


}
```