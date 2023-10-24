#### Parser Content
```Java
{
Name = "microsoft-evsecurity-mix-ds-object-modify-success-4738"
Vendor = "Microsoft"
Product = "Event Viewer - Security"
TimeFormat = ["yyyy-MM-dd'T'HH:mm:ss.SSS", "MM/dd/yyyy hh:mm:ss a"]
Conditions = [
"""A user account was changed"""
]
Fields = [
"""({event_name}A user account was changed)"""
"""({event_code}4738)(<|\s|")"""
"""Computer(Name)?\s*\\*"?(=|:|>)\s*"*(::ffff:)?({host}[\w\.-]+)(\s|,|"|</Computer>|$)"""
"""\sComputerName =(::ffff:)?({host}.+?)(\s+\w+=|\s*$)"""
"""({time}\d\d\/\d\d\/\d\d\d\d \d\d:\d\d:\d\d (am|AM|pm|PM))"""
"""({time}\d+-\d+-\d+T\d+:\d+:\d+\.\d+)"""
"""(?i)\w+\s+\d+\s\d+:\d+:\d+\s+(::ffff:)?(am|pm|({host}[\w\-.]+))\s*Account Expires:"""
"""Security ID:\s*(|({user_sid}[^:]+?))\s+Account Name:"""
"""Account Name:\s*(|({user}[\w\.\-]{1,40}\$?))\s+Account Domain:\s*(|({domain}[^\s:]+?))\s+Logon ID:\s*(|({login_id}[^\s:]+?))\s+Target Account:"""
"""Target\sAccount[\s\S]*?Security ID:\s*({target_sid}[^:]+?)\s"""
"""Target\sAccount[\s\S]*?Account Name:\s*({dest_user}[^\s:]+?)\s"""
"""Target\sAccount[\s\S]*?Account Domain:\s*({dest_domain}[^\s:]+?)\s"""
"""User Account Control:\s*(-|({uac_status}[^:]+?))\s+User Parameters:"""
"""Changed Attributes:\s*(|({attribute}.+?))\s+SAM Account Name"""
"""(?i)\w+\s+\d+\s+\d+:\d+:\d+\s+(::ffff:)?(({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?|(am|pm|({dest_host}[\w\-.]+)))\s*Account Expires:"""
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