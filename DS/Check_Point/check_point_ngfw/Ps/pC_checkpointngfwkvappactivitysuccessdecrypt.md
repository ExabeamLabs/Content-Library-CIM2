#### Parser Content
```Java
{
Name = checkpoint-ngfw-kv-app-activity-success-decrypt
  ParserVersion = "v1.0.0"
  Conditions = [ """Product=VPN-1 & FireWall-1""" , """Action=decrypt""" ]

checkpoint-firewall = {
  Vendor = Check Point
  Product = Check Point NGFW
  TimeFormat = "epoch"
  Fields = [
    """\Wrt=({time}\d{13})""",
    """\Wact=(|({action}.+?))(\s+\w+=|\s*$)""",
    """\Wifname=(|({src_interface}.+?))(\s+\w+=|\s*$)""",
    """\Woriginsicname=(|({user_ou}.+?))(\s+\w+=|\s*$)""",
    """\Wproduct=(|({product_name}.+?))(\s+\w+=|\s*$)""",
    """\Wservice_id=(|({protocol}.+?))(\s+\w+=|\s*$)""",
    """\Wrule_name=(|({rule}.+?))(\s+\w+=|\s*$)""",
    """\Wconn_direction=(|({direction}.+?))(\s+\w+=|\s*$)""",
    """\Wapp=(|({protocol}.+?))(\s+\w+=|\s*$)""",
    """\Wcp_severity=(|({alert_severity}.+?))(\s+\w+=|\s*$)""",
    """\W(s|d)user=({last_name}[^\s]+)\s+({first_name}[^\s]+)\s+-\s+\(({department}[^)]+)\)\s+-\s+({company}[^\s]+)\s+\((({email_address}[^@\s]+@[^)]+)|({user}[^\)]+))""",
    """\W(s|d)user=((CheckPoint|({last_name}[^\s]+))\s+(Firewall|({first_name}[^\s]+))\s+)\((({email_address}[^\s@]+@[^\)]+)|checkpointfw|({user}[^\)]+))""",
    """\Wshost=(|({src_host}[\w\-.]+?)(@({domain}[^\s@]+))?)(\s+\w+=|\s*$)""",
    """\Wsntdom=(|({domain}.+?))(\s+\w+=|\s*$)""",
    """\Wos_name=(|({os}.+?))(\s+\w+=|\s*$)""",
    """\WdestinationTranslatedAddress=(0\.0\.0\.0|({dest_translated_ip}[a-fA-F\d.:]+))""",
    """\WsourceTranslatedAddress=(0\.0\.0\.0|({src_translated_ip}[a-fA-F\d.:]+))""",
    """\Worigin=({origin_ip}[a-fA-F\d.:]+)""",
    """\Wsrc=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
    """\Wdst=({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?""",
    """dvc=({host}[a-fA-F\d.:]+)""",
    """ahost=({host}[^\s]+)""",
    """\Wspt=({src_port}\d+)""",
    """\Wdpt=({dest_port}\d+)""",
    """\Wserver_inbound_bytes=({bytes_in}\d+)""",
    """\Wserver_outbound_bytes=({bytes_out}\d+)""",
    """\Win=({bytes_in}\d+)""",
    """\Wout=({bytes_out}\d+)""",
    """categoryOutcome=(\/)?({result}.+?)\s\w+=""",
    """tunnel_protocol=({tunnel_protocol}[^=]+?)\s*\w+=""",
    """deviceDirection=({direction}[^=]+)\s\w+=""",
    """proto=({protocol}[^=]+?)\s\w+="""
  
}
```