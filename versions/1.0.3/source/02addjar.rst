Add the SDK as a JAR library
============================

If you're running an environment which does not support Gradle, then you'll need to add the SDK manually.

First download and extract the following archive `SAAgeGateSDK-<sdk_version>.Android.jars.zip <https://github.com/SuperAwesomeLTD/sa-sdk-build-repo/blob/master/package/ag_android/<sdk_version>/SAAgeGateSDK-<sdk_version>.Android.jars.zip?raw=true>`_

The archive will contain a number of .jar files, representing the components of the SDK that you'll need to add to the **lib** folder in your Android project.

Then, add the following items in your *AndroidManifest.xml* file, under the Application tag:

.. code-block:: xml

  <activity android:name="tv.superawesome.sdk.agegate.SAAgeGate"
            android:label="SAAgeGate"
            android:configChanges="keyboardHidden|orientation|screenSize"
            android:theme="@android:style/Theme.Holo.Dialog.NoActionBar"
            android:excludeFromRecents="true"/>

  <activity android:name="tv.superawesome.sdk.agegate.SAAgeInput"
            android:theme="@android:style/Theme.Translucent.NoTitleBar"/>

This will register two activities for your application, all needed by the SDK.

Once you've added the Android Age Gate SDK, you can access all functionality by including:

.. code-block:: java

    import tv.superawesome.sdk.agegate.*;
