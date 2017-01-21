Introduction (介绍)
====================

Robot Framework is a Python-based, extensible keyword-driven test
automation framework for end-to-end acceptance testing and
acceptance-test-driven development (ATDD). It can be used for testing
distributed, heterogeneous applications, where verification requires
touching several technologies and interfaces.

Robot Framework 是一种基于 python 的可扩展关键字驱动的自动化测试框架,通常用于端到端的验收测试和验收测试驱动开发。
它可以用于测试声明涉及到多种技术和接口的分布式、异构的应用系统。

The framework has a rich ecosystem around it consisting of various generic
test libraries and tools that are developed as separate projects. For more
information about Robot Framework and the ecosystem, see
http://robotframework.org.

这个框架有丰富的生态系统,包括各种通用的测试库和工具作为单独项目开发。更多资料关于 Robot Framework 和它的生态系统,
请参考: http://robotframework.org 。


Robot Framework is open source software released under the `Apache License
2.0`_. Its development is sponsored by the `Robot Framework Foundation
<http://robotframework.org/foundation>`_.

Robot Framework是在 `Apache License 2.0`_ 许可证下发布的开源软件。它的发展是由 `Robot Framework Foundation
<http://robotframework.org/foundation>`_ 赞助。

.. contents::
   :depth: 2
   :local:

Why Robot Framework? (为何选择Robot Framework?)
-------------------------------------------------

- Enables easy-to-use tabular syntax for `creating test cases (创建测试用例)`_ in a uniform
  way.

- 使用容易使用的表格语法,用统一格式创建测试用例。

- Provides ability to create reusable `higher-level keywords`_ from the
  existing keywords.

- 提供重复利用已经存在的关键字来创建高层次关键字的能力。

- Provides easy-to-read result reports_ and logs_ in HTML format.

- 提供易于阅读结果,采用 HTML 格式的报告和日志。

- Is platform and application independent.

- 平台与被测系统应用程序相互独立。

- Provides a simple `library API`_ for creating customized test libraries
  which can be implemented natively with either Python or Java.

- 提供用于创建自定义测试库的简单库API,它可以使用Python或Java本地实现。

- Provides a `command line interface`__ and XML based `output files`_  for
  integration into existing build infrastructure (continuous integration
  systems).

- 提供命令行界面和基于XML的输出文件,用于集成到现有构建基础架构(持续集成系统)中。

- Provides support for Selenium for web testing, Java GUI testing, running
  processes, Telnet, SSH, and so on.

- 提供对 Selenium 的 Web 测试,Java GUI 测试,运行的支持进程,Telnet,SSH等的支持。

- Supports creating `data-driven test cases`__.

- 支持创建数据驱动测试用例。

- Has built-in support for `variables (变量)`_, practical particularly for testing in
  different environments.

- Built-in 支持不同环境下的特殊变量。

- Provides tagging__ to categorize and `select test cases`__ to be executed.

- 提供标记以对要执行的测试用例进行分类和选择。

- Enables easy integration with source control: `test suites`_ are just files
  and directories that can be versioned with the production code.

- 实现与源代码控制的轻松集成:测试集是可以使用生产代码进行版本化的文件和目录。

- Provides `test-case`__ and `test-suite`__ -level setup and teardown.

- 提供测试用例和测试集级别的 setup 和 teardown。

- The modular architecture supports creating tests even for applications with
  several diverse interfaces.

- 模块化的结构甚至支持为有多种接口的应用程序创建测试数据。

__ `Executing test cases`_
__ `Data-driven style`_
__ `Tagging test cases`_
__ `Selecting test cases`_
__ `Test setup and teardown`_
__ `Suite setup and teardown`_


High-level architecture (高层次的架构)
---------------------------------------

Robot Framework is a generic, application and technology independent
framework. It has a highly modular architecture illustrated in the
diagram below.

Robot Framework 是一个通用的，应用和技术相互独立的框架。它有一个高度模块化的架构图如下。

.. figure:: src/GettingStarted/architecture.png

   Robot Framework architecture (Robot Framework 架构图)

The `test data`_ is in simple, easy-to-edit tabular format. When
Robot Framework is started, it processes the test data, `executes test
cases`__ and generates logs and reports. The core framework does not
know anything about the target under test, and the interaction with it
is handled by `test libraries`__. Libraries can either use application
interfaces directly or use lower level test tools as drivers.

测试数据以一种简单易于编辑的表格格式。当 Robot Framework 启动的时候，启动测试数据，执行测试用例
并且生成日志和报告。核心框架不知道任何关于被测目标系统的细节，核心框架与被测系统通过测试库进行交互。
测试库能够直接使用应用程序接口或者使用更低层次的测试工具作为驱动。

__ `Executing test cases`_
__ `Creating test libraries (创建测试库)`_


Screenshots (屏幕截图)
-----------------------

Following screenshots show examples of the `test data`_ and created
reports_ and logs_.

以下屏幕截图展示了测试数据和创建的报告和日志的例子。

.. figure:: src/GettingStarted/testdata_screenshots.png

   Test case files (测试用例文件)

.. figure:: src/GettingStarted/screenshots.png

   Reports and logs (报告和日志)


Getting more information (获取更多信息)
----------------------------------------

Project pages (项目页面)
~~~~~~~~~~~~~~~~~~~~~~~~~

The number one place to find more information about Robot Framework
and the rich ecosystem around it is http://robotframework.org.
Robot Framework itself is hosted on GitHub__.

查找有关 Robot Framework 的更多信息和它周围的丰富的生态系统,首要的地方是 http://robotframework.org。
Robot Framework 本身托管在 GitHub 上。

__ https://github.com/robotframework/robotframework

Mailing lists (邮件列表)
~~~~~~~~~~~~~~~~~~~~~~~~~

There are several Robot Framework mailing lists where to ask and
search for more information. The mailing list archives are open for
everyone (including the search engines) and everyone can also join
these lists freely. Only list members can send mails, though, and to
prevent spam new users are moderated which means that it might take a
little time before your first message goes through.  Do not be afraid
to send question to mailing lists but remember `How To Ask Questions
The Smart Way`__.

这里有几个 Robot Framework 邮件列表可以提问和搜索更多信息。
邮件列表档案对每个人（包括搜索引擎）都是开放的,每个人都可以自由加入这些列表。
只有列表成员可以发送电子邮件,为了防止垃圾邮件,新用户需要被审核，
这意味着它在你的第一条消息通过之前可能需要一个很少的时间。
不要害怕发送问题到邮件列表，但要记住提问的技巧。

robotframework-users__
   General discussion about all Robot Framework related
   issues. Questions and problems can be sent to this list. Used also
   for information sharing for all users.

   通常讨论关于 Robot Framework 相关的问题。疑问和难题都可以发送到这个邮件列表。所有用户将分享这些信息。

robotframework-announce__
    An announcements-only mailing list where only moderators can send
    messages. All announcements are sent also to the
    robotframework-users mailing list so there is no need to join both
    lists.

    一个只读公告邮件列表仅有管理员能够发送消息。所有公告被发送到 Robot Framework 的用户邮件列表当中,
    所以没必要同时加入两个列表中。

robotframework-devel__
   Discussion about Robot Framework development.

   讨论关于 Robot Framework 的开发。

__ http://www.catb.org/~esr/faqs/smart-questions.html
__ http://groups.google.com/group/robotframework-users
__ http://groups.google.com/group/robotframework-announce
__ http://groups.google.com/group/robotframework-devel
