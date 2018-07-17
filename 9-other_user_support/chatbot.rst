=================
创建聊天机器人
=================

:date: 2018-06-06 


商业解决方案：
* https://www.luis.ai



课程演示：

1. 开源聊天机器人： `ChatterBot <http://chatterbot.readthedocs.io>`_
2. 微信接口： `wxpy <http://wxpy.readthedocs.io/zh/latest/>`_


 .. code-block:: python

    #!/usr/bin/env python3.5
    from wxpy import *
    from chatterbot import ChatBot
    from chatterbot.trainers import ChatterBotCorpusTrainer


    chatbot = ChatBot("gzj")# 用于回复消息的机器人
    chatbot.set_trainer(ChatterBotCorpusTrainer)
    chatbot.train("chatterbot.corpus.chinese")# 使用该库的中文语料库
    bot = Bot(cache_path=True)# 用于接入微信的机器人
    group_2 = bot.groups("技术传播方法")[0]# 进行测试的群

    #group_2.send("大家好，我是人工智障")
    hjy=bot.friends().search('京燕')[0]
    @bot.register(hjy)
    def reply_my_friend(msg):
        return chatbot.get_response(msg.text).text

    @bot.register(group_2)
    def reply_my_friend(msg):
        if msg.is_at:
            return chatbot.get_response(msg.text).text# 使用机器人进行自动回复
    # 堵塞线程，并进入 Python 命令行
    embed()


