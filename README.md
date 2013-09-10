How to use RobotFramework with the Selenium Library
Posted on July 26, 2011 by admin	

    digg
    Sharebar

RobotFramework logo

At Wallix we use RobotFramework to test our products AdminBastion and LogBox in a black box way mainly for exercising the web interface. In this blog post we’ll explain one way of using RobotFramework to test web interfaces either for web site testing or for web application testing.
What is RobotFramework ?

Robot Framework is a generic test automation framework for acceptance testing. It has an easy-to-use tabular test data syntax and utilizes a keyword-driven testing approach. Its testing capabilities can be extended by test libraries implemented either with Python or Java, and users can create new keywords from existing ones using the same syntax that is used for creating test cases.

 Robot Framework is an open source software released under the Apache License 2.0. It’s developed and owned by Nokia Siemens Networks.

For more information in order to install and setup RobotFramework, you should read the RobotFramework Wiki and the Setup and installation page.

What is the Selenium Library ?

The Selenium Library is a RobotFramework test library that uses the popular Selenium web testing tool internally. It provides a powerful combination of a simple test data syntax and support for different browsers.
Objective of this Tutorial

The objective of this tutorial is to explain how to use RobotFramework with Selenium and to detail some functionalities of RobotFramework by the way.
Pre-conditions

    Install RobotFramework on your machine: ( python setup.py install ), for Windows environment you have to install python 2.7.
    Then, you have to get the Java Runtime Environment (JRE) for running the Selenium Server.
    Make sure you have Firefox in your path.
    Install the Selenium Library using: python setup.py install

For Windows environment you can use the windows installer.
Getting started

First, you have to launch the Selenium server. In a terminal go to your directory where selenium-server.jar file are present and launch the server by typing :

[mbu@mbu2 poc]$ cd <my selenium server directory>
[mbu@mbu2 poc]$ java -jar selenium-server.jar

Your Selenium server should start …You can specify more options, like port, firefox profile etc…

Now you can write your first test. This test will open a browser to www.google.fr web site and type selenium in the search area.

Before writing your first test make sure that the command pybot –help works well.

There are different ways to write a test with RobotFramework. You can write your test in an html file using a table, in a standard text file or in a rst file. In this tutorial, we will use a standard text file.

So, now you can make a directory for your first test: