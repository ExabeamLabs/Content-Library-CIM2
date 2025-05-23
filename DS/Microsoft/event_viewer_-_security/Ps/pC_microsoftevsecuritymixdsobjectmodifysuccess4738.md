#### Parser Content
```Java
{
Name = "microsoft-evsecurity-mix-ds-object-modify-success-4738"
Vendor = "Microsoft"
Product = "Event Viewer - Security"
TimeFormat = ["yyyy-MM-dd'T'HH:mm:ss.SSS", "MM/dd/yyyy hh:mm:ss a", "yyyy-MM-dd'T'HH:mm:ss.SSSSSSSZ", "yyyy-MM-dd'T'HH:mm:ss"]
Conditions = [
"""A user account was changed"""
]
Fields = [
"""({event_name}A user account was changed)"""
"""({event_code}4738)(<|\s|"|\|)"""
"""({event_code}\d+)\|\s+devTime=({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)"""
"""Computer(Name)?\s*\\*"?(=|:|>)\s*"*(::ffff:)?({host}[\w\.-]+)(\s|,|"|</Computer>|$)"""
"""\sComputerName =(::ffff:)?({host}.+?)(\s+\w+=|\s*$)"""
"""({time}\d\d\/\d\d\/\d\d\d\d \d\d:\d\d:\d\d (am|AM|pm|PM))"""
"""({time}\d+-\d+-\d+T\d+:\d+:\d+\.\d+)"""
"""TimeGenerated":"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d\d\d\d\d\d\dZ)""""
"""(?i)\w+\s+\d+\s\d+:\d+:\d+\s+(::ffff:)?(am|pm|\d{4}|({host}[\w\-.]+))\s*Account Expires:"""
"""Security ID:\s*(|({user_sid}[^:]+?))\s+Account Name:"""
"""Account Name:\s*(|({user}[\w\.\-\!\#\^\~]{1,40}\$?))\s+Account Domain:\s*(|({domain}[^\s:]+?))\s+Logon ID:\s*(|({login_id}[^\s:]+?))\s+Target Account:"""
"""Target\sAccount[\s\S]*?Security ID:\s*({dest_user_sid}[^:]+?)\s"""
"""Target\sAccount[\s\S]*?Account Name:\s*({dest_user}[^\s:]+?)\s"""
"""Target\sAccount[\s\S]*?Account Domain:\s*({dest_domain}[^\s:]+?)\s"""
"""User Account Control:\s*(-|({uac_status}[^:]+?))\s+User Parameters:"""
"""Changed Attributes:\s*(|({attribute}.+?))\s+SAM Account Name"""
"""(?i)\w+\s+\d+\s+\d+:\d+:\d+\s+(::ffff:)?(({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?|(am|pm|\d{4}|({dest_host}[\w\-.]+)))\s*Account Expires:"""
""""agent.id":"({agent_id}\d+)"""
""""location":"({log_location}[^"]+)"""
""""decoder.name":"({decoder_name}[^"]+)"""
""""decoder.name":"({decoder_name}[^"]+)"""
""""data.data":"({data}[^"]+)"""
""""manager.name":"({wazuh_manager}[^"]+)"""
""""rule.description":"({description}[^"]+)"""
""""path":"({log_path}[^"]+)"""
"""<Data Name\\*='TargetSid'>({dest_user_sid}[^<]+)"""
"""<Data Name\\*='OldUacValue'>({old_attribute}[^<]+)"""
"""<Data Name\\*='NewUacValue'>({new_attribute}[^<]+)"""
]
ParserVersion = "v1.0.0"


}
```