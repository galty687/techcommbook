XML
##############

:date: 2018-05-08
:author: 高志军



XML是非常重要的存储数据的方式，作为技术写作从业人员，需要了解XML的基本技术，具体如下：

* XML
* CSS/XSLT
* DTD/Schema


创建XML
================

 .. code-block:: xml

    <?xml version="1.0"?>

    <BusinessCard>
        <Name>Gao Zhijun</Name>
        <phone type="mobile">+86 10 8264 9812</phone>
        <phone type="work">+86 10 6127 3510</phone>
        <phone type="fax">+86 10 6127 3510</phone>
        <email>gaozhijun@ss.pku.edu.cn</email>
    </BusinessCard>



创建CSS
=======================

 .. code-block:: css

    BusinessCard {
        font-family: Arial, Helvetica, sans-serif;
        background-color: #DACFE5;
        width: 300px;
        display: block;
        padding: 10pt;
        border: 1px solid #0D3427;
        margin: 5px;
        text-align: left;
    }

    Name {
        color: #0D3427;
        font-weight: bold;
        font-size: 140%;
        display: block;
        margin-bottom: 3%;
    }

    phone {
        font-size: 90%;
        color: #523819;
        font-size: 90%;
        display: block;
    }

    email {
        color: #0D3427;
        font-size: 90%;
        font-weight: bold;
        display: block;
        margin-top: 3%;
    }


关联CSS至XML

::

    <?xml-stylesheet type="text/css" href="businesscard.css"?>



创建页面内DTD
=================

 .. code-block:: html

    <!DOCTYPE BusinessCard [
    <!ELEMENT BusinessCard (Name, phone+, email?)>
    <!ELEMENT Name (#PCDATA)>
    <!ELEMENT phone (#PCDATA)>
    <!ATTLIST phone type (mobile | fax | Work | home) #REQUIRED>

    <!ELEMENT emai (#PCDATA)>
    
    ]>

DTD 参考：https://www.w3cschool.cn/dtd/dtd-intro.html


.. note::

    * #PCDATA (Parsed Character Data)，简单解释就是元素内只有文本，没有子元素。



创建独立DTD并关联至xml
=======================

::

    <!DOCTYPE BusinessCard SYSTEM "businesscard.dtd">

