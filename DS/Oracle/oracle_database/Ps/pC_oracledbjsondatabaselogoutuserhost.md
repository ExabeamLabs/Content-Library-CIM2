#### Parser Content
```Java
{
Name = oracle-db-json-database-logout-userhost
  Vendor = Oracle
  Product = Oracle Database
  ParserVersion = "v1.0.0"
  TimeFormat ="yyyy-MM-dd'T'HH:mm:ss.SSSZ"
  Conditions = [ """action_name""", """LOGOFF""", """os_username""", """userhost""" ]
  Fields=[
    """"os_username":"({user}[\w\.\-]{1,40}\$?)"""
    """"username":"({db_user}[^"]+)"""
    """"action_name":"({operation}[^"]+)""",
    """"sessionid":"({session_id}[^"]+)""",
    """"userhost":"(([^\\]+)[\\]+)?({host}[^"]+)"""",
    """"os_process":"({process_id}[^"]+)""",
    """timestamp":"({time}[^"]+)""",
    """"exa_jdbc_database":"({db_name}[^"]+)""",
    """"priv_used":"({additional_info}[^"]+)"""",
    """"exa_jdbc_type":"({app}[^"]+)"""",
    """"exa_jdbc_hostname":"({dest_host}[^"]+)"""",
    """"exa_jdbc_port":"({dest_port}\d+)""""
  ]


}
```