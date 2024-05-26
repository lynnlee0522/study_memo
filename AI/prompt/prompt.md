### prompt 如何写出更好的prompt

###### LLM 分类
- Base LLM
- Instruction Tuned LLM

###### 编写prompt的关键原则
- 编写明确和具体的指令
  - 使用分隔符清楚地指示输入的不同部分
    - triple quotes: '''
    - triple backticks: ```
    - angle brackets: < >
    - xml tags: <tag> </tag>
    >示例prompt:  summarize the text delimited by triple backticks \```{text}\```
  - 要求结构化输出 
    >示例prompt:  provide them in JSON format with the following keys: kook_id, title
  - 要求模型检查是否满足条件
    >示例prompt: check assumptions required todo the task
  - 提供成功执行任务的示例
  
- 给模型足够的时间来思考
  - 指定完成任务所需的步骤
    >示例prompt: 
    1. summarize the following text by <> with 1 sentence 
    2.translate the summary into French  
    3.output a json object
  - 指示模型在作出结论之前推理出自己的解决方案，可以获得更好的结果
        >示例prompt:  1. Dont't decide if the student's solution is correct until you have done the problem yourself

- 减少幻觉
  - 要求模型首先从文本中找到任何相关的引用
      >示例prompt:  first find relvant information, then answer the question , based on the relevant information.   
 

 ###### 聊天机器人
 ![alt text](image.png)