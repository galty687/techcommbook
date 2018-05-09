=============
DITA快速入门
=============

官网说明：https://docs.oasis-open.org/dita/v1.0/archspec/topicover.html


General Topic
=================

 .. code-blcok:: xml
    
    <topic id="topic">
    <title>Some little topic</title>
    <body>
        <p>Here's a little topic.</p>
        <ul>
        <li>Some item</li>
        <li>Another item</li>
        </ul>
    </body>
    </topic>




Concept Topic

 .. code-block:: xml

    <concept id="concept">
    <title>Bird Calling</title>
        <conbody>
        <p>Bird calling attracts birds.</p>
        <example>
        <p>Bird calling requires learning:</p>
        <ul>
            <li>Popular and classical bird songs</li>
            <li>How to whistle like a bird</li>
        </ul>
        </example>
        </conbody>
    </concept> 



Task Topic

  .. code-block:: xml

    <task id="ertx">
    <title>Creating an ERTX file</title>
        <taskbody>
        <context>Each morning before breakfast you need to 
        create a fresh ERTX file.</context>
        <steps>
        <step><cmd>Start ERTX.</cmd></step></steps>
        <step><cmd>Click New ERTX File.</cmd></step></steps>
        </steps>
        <result>You now have your ERTX file for today!</result>
        </taskbody>
    </task>

Reference Topic

      .. code-block:: xml

            <reference id = "boldproperty">
            <title>Bold property</title>
            <shortdesc>(Read-write) Whether to use a bold font for the specified
            text string.</shortdesc>
            <refbody>
            <refsyn>
                <synph>
                <var>object</var><delim>.</delim><kwd>Font</kwd><delim>.</delim>
                <kwd>Bold</kwd><delim> = </delim><var>trueorfalse</var>
                </synph>
            </refsyn>
            <properties>
                <property>
                <proptype>Data type</proptype>
                <propvalue>Boolean</propvalue>
                </property>
                <property>
                <proptype>Legal values</proptype>
                <propvalue>True (1) or False (0)</propvalue>
                </property>
            </properties>
            </refbody>
            </reference>



DITA MAP

 .. code-block:: xml

        <topicref href="A.dita" collection-type="sequence">
        <topicref href="A1.dita"/>
        <topicref href="A2.dita"/>
        </topicref>
        <reltable>
        <relrow>
            <relcell>A.dita</relcell>
            <relcell>B.dita</relcell>
        </relrow>
        </reltable>


task.dita
============

 .. code-block:: xml

        <?xml version="1.0" encoding="utf-8"?>
        <!DOCTYPE task PUBLIC "-//OASIS//DTD DITA Task//EN" "task.dtd">

        <task xml-lang="zh-cn" id="howToRplace">
        <title>如何更换灶台电池</title>
        <shortdesc>介绍如何快速的更换燃气灶头的电池。</shortdesc>
        <prerequisite>务必需要关上阀门</prerequisite>

        <taskbody>
            <steps>
                <step>
                    <cmd>打开电池盒</cmd>
                </step>
                <step>
                    <cmd>去除旧电池</cmd>
                </step>
                    <step>
                    <cmd>装上新电池</cmd>
                </step>
                <step>
                    <cmd>合上电池盖</cmd>
                </step>
            </steps>
            <result>可以成功打火。</result>
        </taskbody>
        </task>


concept.dita
=================




DITA OT 
=================

发布命令： ``bin/dita --input=sourfile --format=pdf``