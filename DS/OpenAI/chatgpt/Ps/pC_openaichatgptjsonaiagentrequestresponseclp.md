#### Parser Content
```Java
{
Name = openai-chatgpt-json-ai-agent-request-response-clp
  ParserVersion = "v1.0.0"
  Vendor = OpenAI
  Product = ChatGPT
  ExtractionType = json
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSSSSZ"
  Conditions = [ """"type":"CHATGPT_WORKSPACE"""", """"type":"CONVERSATION_MESSAGE"""", """"conversation":""" ]
  Fields = [
    """exa_json_path=$.principal.id,exa_field_name=workspace_id"""
    """exa_json_path=$.timestamp,exa_field_name=time"""
    """exa_json_path=$.conversation.id,exa_field_name=conversation_id"""
    """exa_json_path=$.conversation.gpt_id,exa_field_name=ai_agent_id"""
    """exa_json_path=$.conversation.title,exa_field_name=additional_info"""
    """exa_json_path=$.actor.user_email,exa_field_name=email_address"""
    """exa_json_path=$.actor.user_id,exa_field_name=user_id"""
    """exa_json_path=$.type,exa_field_name=event_name"""
    """exa_json_path=$.message.author.type,exa_field_name=message_author_type"""
    """exa_json_path=$.message.content.value,exa_field_name=llm_request"""
    """exa_json_path=$.message.author.tools_used,exa_field_name=ai_tool_name"""
    """exa_json_path=$.message.files[*].name,exa_field_name=file_name"""
    """exa_json_path=$.message.files[*].id,exa_field_name=file_id"""
    """exa_json_path=$..action_name,exa_field_name=ai_function_name"""
    """exa_json_path=$.message.content.annotations[*].action_name,exa_field_name=ai_function_name"""
    ]


}
```