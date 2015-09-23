# POSHI-TUTORIAL

Welcome to the Poshi Tutorial.

You will receive an introduction to the wonderful world of poshi.

## Quick Steps to Write a Poshi Test

You can follow these steps to create a new article and contribute it from
GitHub.

1.  Make a folder called 'poshi-demo' with a folder inside of it called 'src'.

<img src="" />


2.  Write a gradle file that will deal with downloading and running poshi tests.

<pre>&lt;definition&gt;
  &lt;command name="click"&gt;
    &lt;execute selenium="waitForVisible" argument1="${locator1}" /&gt;
    &lt;execute selenium="click" argument1="${locator1}" /&gt;
  &lt;/command&gt;
&lt;/definition&gt;</pre>


3.  Write 2 function files that will be used in the poshi test.

<pre>&lt;definition&gt;
  &lt;command name="click"&gt;
    &lt;execute selenium="waitForVisible" argument1="${locator1}" /&gt;
    &lt;execute selenium="click" argument1="${locator1}" /&gt;
  &lt;/command&gt;
&lt;/definition&gt;</pre>

4.  Write 1 testcase file that will run the poshi test.

5.  Run the poshi test using the following command:

<pre>gradle runPoshi -PposhiTestName=Smoke</pre>

Congratulations! You've written your first poshi test!

To find out more about Poshi, why we wrote it, and how to use it please continue on in this tutorial!