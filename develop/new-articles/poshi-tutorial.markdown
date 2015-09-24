# POSHI-TUTORIAL

Welcome to the Poshi Tutorial.

You will receive an introduction to the wonderful world of poshi.

## Quick Steps to Write a Poshi Test

You can follow these steps to create a new article and contribute it from
GitHub.

1.  Make a folder called 'poshi-demo' with a folder inside of it called 'src'.

    <h5>/home/liferay/Documents/poshi-demo/test/</h5>

    <img src="../../develop/tutorials/images/poshi-folder-structure-1.png" />

2.  Write a gradle file that will deal with downloading and running poshi tests.

    <h5>/home/liferay/Documents/poshi-demo/build.gradle</h5>

    <pre>buildscript {
        repositories {
          maven {
            url "http://cdn.repository.liferay.com/nexus/content/groups/public"
          }
        }

        dependencies {
          classpath group: "com.liferay", name: "com.liferay.gradle.plugins.poshi.runner", version: "1.0.8"
        }
      }

      repositories {
        mavenLocal()

        maven {
          url "http://cdn.repository.liferay.com/nexus/content/groups/public"
        }
      }

      apply plugin: "com.liferay.poshi.runner"

      poshiRunner {
        version = "1.0.18"
      }</pre>


3.  Write 3 files that will be used in the poshi test.

    <h5>/home/liferay/Documents/poshi-demo/test/Smoke.function</h5>

    <pre>&lt;definition component-name="smoke"&gt;
      &lt;command name="smoke"&gt;
        &lt;execute function="Open" locator1="https://www.liferay.com/" /&gt;
        &lt;execute function="Click" locator1="//a[contains(.,'Products')]" /&gt;
        &lt;execute function="Click" locator1="//a[contains(.,'Features')]" /&gt;
      &lt;/command&gt;
    &lt;/definition&gt;</pre>

    <h5>/home/liferay/Documents/poshi-demo/test/Click.function</h5>

    <pre>&lt;definition default="click"&gt;
      &lt;command name="click"&gt;
        &lt;execute selenium="waitForVisible" /&gt;
        &lt;execute selenium="click" /&gt;
      &lt;/command&gt;
    &lt;/definition&gt;</pre>

    <h5>/home/liferay/Documents/poshi-demo/test/Open.function</h5>

    <pre>&lt;definition default="open"&gt;
      &lt;command name="open"&gt;
        &lt;execute selenium="open" /&gt;
      &lt;/command&gt;
    &lt;/definition&gt;</pre>

4.  Run the poshi test using the following command:

   <pre>gradle runPoshi -PposhiTestName=Smoke</pre>

Congratulations! You've written your first poshi test!

To find out more about Poshi, why we wrote it, and how to use it please continue on in this tutorial!