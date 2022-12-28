#### Parser Content
```Java
{
Name = microsoft-evsecurity-kv-endpoint-login-fail-4625-3
  ParserVersion = v1.0.0
    Vendor = Microsoft
    Product = Event Viewer - Security
    TimeFormat = "MMM dd HH:mm:ss yyyy"
    Conditions = [ """,4625,Microsoft-Windows-Security-Auditing""", """Logon Type""", """An account failed to log on""" ]
    Fields = [
      """({event_name}An account failed to log on)""",
      """,\w+ ({time}\w+ \d+ \d+:\d+:\d+ \d\d\d\d),4625,""",
      """,(Audit Failure|Failure Audit|Information),({dest_host}[^,]+),""",
      """({event_code}4625)""",
      """\s*Subject:.+?Account Name:\s+(?=\w)(-|({src_user}[^\s@]+?))[\s;]*Account Domain:""",
      """\s*Subject:.+?Account Domain:\s+(?=\w)({src_domain}[^:;]+?)[\s;]*Failure Information:""",
      """Logon Type:\s+({login_type}\d+)""",
      """Logon Process:\s+(?:({auth_process}[^\s]+))\s+Authentication Package:""",
      """Authentication Package:\s+(?:({auth_package}[^\s]+))\s+Transited Services""",
      """Logon ID:\s+({login_id}[^\s]+)\s+Logon GUID""",
      """\s*Account For[\s;]*Which Logon Failed:[\s;]*Security ID:\s*(?:\/?NULL SID|(?:|({user_sid}.+?)))[\s;]*Account Name""",
      """\s*Logon Failed:.+?Account Name:\s*(?=\w)({user}[^\s@]+?)[\s;]*Account Domain:""",
      """\s*Logon Failed:.+?Account Domain:\s*(?=\w)({domain}.+?)[\s;]*Failure Information""",
      """\s*Sub Status:\s*({result_code}.+?)[\s;]*Process Information:""",
      """Workstation Name:\s+({src_host_windows}[^\s]+)\s+Source Network""",
      """Source Network Address:\s+(?:-|({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?)\s+Source Port:"""
      """Key Length:\s*({key_length}\d+)"""
    ]
    DupFields = [ 
      "dest_host->host" 
      "result_code->failure_code"
    ]
  

}
```