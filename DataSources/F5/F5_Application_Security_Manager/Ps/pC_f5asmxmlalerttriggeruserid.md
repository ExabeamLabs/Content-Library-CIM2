#### Parser Content
```Java
{
Name = f5-asm-xml-alert-trigger-userid
  ParserVersion = v1.0.0
  Vendor = F5
  Product = F5 Application Security Manager
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Conditions = [ """ ASM:""", """HTTPS""", """<USERID>"""]
  Fields = [
    """\w+\s+\d+\s+\d\d:\d\d:\d\d\s+({host}[^\s]+)\s+ASM:""",
    """\sASM:"[^"]*","({time}\d\d\d\d-\d\d-\d\d \d\d:\d\d:\d\d)""",
    """\sASM:("[^"]*",){2}"({dest_ip}[\da-fA-F\.:]+)""",
    """\sASM:("[^"]*",){3}"({src_ip}[\da-fA-F\.:]+)""",
    """\sASM:("[^"]*",){4}"({method}[^"]+)""",
    """\sASM:("[^"]*",){5}"({protocol}[^"]+)"""",
    """\sASM:("[^"]*",){8}"({additional_info}[^"]+)"""",
    """\sASM:("[^"]*",){8}"({alert_name}[^"]+)"""",
    """\sASM:"({alert_name}[^"]+)"""",
    """\sASM:("[^"]*",){9}"(?:N\/A|({user}[^"]+))"""",
    """\sASM:("[^"]*",){13}"\w+\s+({malware_url}[^"]+?)(?:\s+\w+\/\d\.\d|)((\\r\\n|\s+)[\w\-]+:|")""",
    """Host:\s*({domain}[^"\\]+?)(\\r|\\n|\s+|\\t)""",
    """User-Agent:\s*({user_agent}[^"]+?)(\\r\\n[\w\-]+:|")""",
    """User-Agent:\s*Mozilla\/.+?({browser}Chrome|Safari|Opera|(?:F|f)irefox|MSIE|Trident)""",
    """<USERID>({user_id}[^\\\<]+)""",
# user_pass is removed
# bank_id is removed
    """<ACCTID>({account_id}[^\\\<]+)""",
    """<ACCTTYPE>({user_type}[^\\\<]+)""",
  ]
  DupFields = ["protocol->alert_type"]


}
```