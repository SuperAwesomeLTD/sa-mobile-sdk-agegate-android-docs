Add the SDK through Gradle
==========================

The simplest way of adding the Android Age Gate SDK to your Android Studio project is to download the AAR library through Gradle.

The first step is to include the following Maven repository in your module's **build.gradle** file (usually the file under MyApplication/app/):

.. code-block:: shell

    repositories {
        maven {
            url  'http://dl.bintray.com/gabrielcoman/maven'
        }
    }

Next you need to add the following dependency:

.. code-block:: shell

    dependencies {
      compile 'compile 'tv.superawesome.sdk.agegate:saagegate:<sdk_version>'
    }

Once you've added the Android Age Gate SDK, you can access all functionality by including:

.. code-block:: java

    import tv.superawesome.sdk.agegate.*;
